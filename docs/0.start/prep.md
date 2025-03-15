# Before you begin

#### Choose a domain name or subdomain name for your server

Hubzilla can only be installed into the root of a domain or sub-domain, and can
not be installed using alternate TCP ports.

#### Decide if you will use SSL and obtain an SSL certificate before software installation

You SHOULD use SSL. If you use SSL, you MUST use a "browser-valid" certificate.
*You MUST NOT use self-signed certificates!*

Please test your certificate prior to installation. A web tool for testing your
certificate is available at "http://www.digicert.com/help/". When visiting your
site for the first time, please use the SSL ("https://") URL if SSL is available.
This will avoid problems later. The installation routine will not allow you to
use a non browser-valid certificate.

This restriction is incorporated because public posts from you may contain
references to images on your own hub. Other members viewing their stream on
other hubs will get warnings if your certificate is not trusted by their web
browser. This will confuse many people because this is a decentralised network
and they will get the warning about your hub while viewing their own hub and may
think their own hub has an issue. These warnings are very technical and scary to
some folks, many of whom will not know how to proceed except to follow the browser
advice. This is disruptive to the community. That said, we recognise the issues
surrounding the current certificate infrastructure and agree there are many
problems, but that doesn't change the requirement.

Free "browser-valid" certificates are available from providers such as StartSSL
and LetsEncrypt.

If you do NOT use SSL, there may be a delay of up to a minute for the initial
install script - while we check the SSL port to see if anything responds there.
When communicating with new sites, $Projectname always attempts connection on the
SSL port first, before falling back to a less secure connection.  If you do not
use SSL, your webserver MUST NOT listen on port 443 at all.

If you use LetsEncrypt to provide certificates and create a file under
.well-known/acme-challenge so that LetsEncrypt can verify your domain ownership,
please remove or rename the .well-known directory as soon as the certificate is
generated. $Projectname will provide its own handler for ".well-known" services when
it is installed, and an existing directory in this location may prevent some of
these services from working correctly. This should not be a problem with Apache,
but may be an issue with nginx or other web server platforms.
