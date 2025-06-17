# Utsukta Hub Documentation

## Welcome to Utsukta Hub

You’ve arrived at the official documentation for Utsukta Hub, a Hubzilla-powered community designed to connect people securely and privately. Whether you’re a new user, an administrator, or a developer, this is your one-stop resource for getting started, managing your experience, and diving into the technical details.

## What is Hubzilla?

Hubzilla is a decentralised communication network with the aim of providing communication options that circumvent censorship, respect privacy and are therefore free from the restrictions imposed by today's commercial communication giants. These primarily provide spy networks for paying customers of all kinds and monopolise and centralise the entire Internet - which was not originally among the revolutionary goals that led to the World Wide Web.

Hubzilla is free, open source and free of charge. It was developed to run on a Raspberry Pi as well as on the largest AMD and Intel Xeon multiprocessor servers. It can be used for communication between a few individuals or connect many thousands of people and more.

Another goal is to be independent of skills and resources. Hubzilla is as easy to use for the ordinary computer user as it is for system administrators and developers.

Hubzilla is written in PHP, making it easy to install on any of today's hosting platforms, including self-hosting at home, on shared servers or on virtual and dedicated servers.

## Hubzilla Timeline and History

### 15 Years of Innovation

**Collaborate, Innovate, and Cross-Pollinate**

Hubzilla and its predecessors are pioneers of the fediverse, bringing cutting-edge features and innovation to decentralized social media. This includes tireless work from fediverse pioneer Mike Macgirvin, Hubzilla head developer Mario Vavti, as well as many many other contributors.

Hubzilla traces its roots to 2010 with the release of Mistpark created by Mike Macgirvin, and became an independent project in 2012, being called Red and then Red Matrix before being called Hubzilla. The Hubzilla community took over the project in early 2015, and the Hubzilla Association was created in 2023.

This is a team effort, with lots of contributors, both from within and without Hubzilla. Special thanks to other platforms, such as (streams), Forte, and others who collaborate, innovate, and cross-pollinate.

#### Major Milestones

| Date        | Event Description                                                                                                                                                                                                                              |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 14 May 2025 | 15 Year Anniversary                                                                                                                                                                                                                            |
| May 2025    | Hubzilla website redesigned (in progress).                                                                                                                                                                                                     |
| 21 Dec 2024 | **Hubzilla 10** released. <ul><li>Implementation of **Conversation Containers over ActivityPub**, enhancing threaded conversation backfill and moderation tools. Initially released in (streams), then in Hubzilla.<sup>5</sup></li></ul>      |
| 23 Nov 2024 | **FEP-171b: Conversation Containers** and related specifications submitted as Fediverse Enhancement Proposals (FEPs), thanks to silverpill.<sup>1</sup>                                                                                        |
| 22 Mar 2024 | **Hubzilla 9** released.                                                                                                                                                                                                                       |
| 7 Feb 2024  | **FEP-61cf: The OpenWebAuth Protocol**, enabling federated single sign-on, submitted as an FEP, thanks to FenTiger.<sup>1</sup>                                                                                                                |
| 29 Nov 2023 | <img src="https://hubzilla.org/cloud/info/website_images_small/hz-16.png" alt="Hubzilla logo" class="me-1"> [**Hubzilla Association**](https://hubzilla.org/page/info/association) established.                                                |
| 23 Jun 2023 | **Hubzilla 8.4.2** released. <ul><li>Updated to Bootstrap 5.3.0 (stable version).</li></ul>                                                                                                                                                    |
| 13 Jan 2023 | **Hubzilla 8** released.                                                                                                                                                                                                                       |
| 22 Oct 2022 | **Hubzilla 7.8** released. <ul><li>Updated to Bootstrap 5.2 with CSS variables.</li></ul>                                                                                                                                                      |
| 21 Jan 2022 | **Hubzilla 7** released.                                                                                                                                                                                                                       |
| 25 May 2021 | GNU Social addon, enabling OStatus protocol, retired. OStatus no longer supported.                                                                                                                                                             |
| 8 Sep 2021  | **Hubzilla 6.2** released. <ul><li>Made Hubzilla installable as a **Progressive Web App (PWA)**.</li><li>Updated to Bootstrap 5.</li></ul>                                                                                                     |
| 9 Jul 2021  | **Hubzilla 6** released. <ul><li>Implemented **desktop notifications**.</li><li>Zot no longer supported; Zot6 required. ActivityPub, OStatus, and Diaspora still supported.</li></ul>                                                          |
| 5 Nov 2020  | **Hubzilla 5** released. <ul><li>Switched to **Zot6** as primary protocol; Zot, ActivityPub, OStatus, and Diaspora supported.</li><li>Implemented **calendar syncing** using DAV and nomadic identity.</li><li>Introduced **polls**.</li></ul> |
| 3 Mar 2019  | **Hubzilla 4** released. <ul><li>Upgraded from Zot to **Zot6**; Zot supported for compatibility.</li></ul>                                                                                                                                     |
| 2019        | Re-implemented the **Zot Protocol** to use ActivityStreams2 content.<sup>1</sup>                                                                                                                                                               |
| 17 Aug 2018 | _Zap and Osada released with **Zot6** support._<sup>1</sup> _Osada and Zap are forks of Hubzilla._<sup>5</sup>                                                                                                                                 |
| 9 Mar 2018  | **Hubzilla 3.2** released. <ul><li>Upgraded from Bootstrap 4 beta to stable.</li></ul>                                                                                                                                                         |
| 9 Jan 2018  | **Hubzilla 3** released.                                                                                                                                                                                                                       |
| 23 Jan 2018 | _ActivityPub became a W3C Recommendation (web standard)._<sup>1</sup>                                                                                                                                                                          |
| 25 Oct 2017 | **Hubzilla 2.8** released. <ul><li>Implemented **OpenWebAuth**, replacing Magic Auth.</li><li>Preparations for **Zot6** upgrade began.</li></ul>                                                                                               |
| 2017        | Magic Auth separated from Zot, becoming **OpenWebAuth (OWA)** for broader adoption.<sup>4</sup>                                                                                                                                                |
| 10 Sep 2017 | _Mastodon added ActivityPub in v1.6.0, replacing OStatus._<sup>1</sup> Hubzilla and Mastodon began using ActivityPub for communication.                                                                                                        |
| 30 Jul 2017 | PubCrawl addon created, adding **ActivityPub** as an additional protocol.                                                                                                                                                                      |
| 31 May 2017 | **Hubzilla 2.4** released. <ul><li>Supported reverse Magic Auth in Oembed requests.</li><li>Redbasic theme updated to Bootstrap 4.</li></ul>                                                                                                   |
| 2017        | _Mike Macgirvin demonstrated first **ActivityPub** posts/comments federating._<sup>1</sup>                                                                                                                                                     |
| 23 Dec 2016 | **Hubzilla 2** released.                                                                                                                                                                                                                       |
| 2016        | Implemented **private groups**.                                                                                                                                                                                                                |
| 16 Mar 2016 | _Mastodon arrived, federating with Hubzilla via OStatus._<sup>1</sup>                                                                                                                                                                          |
| 2016        | Provided **(sanitised) inline SVG support** for quick doodles/drawings in posts.                                                                                                                                                               |
| 3 Dec 2015  | **Hubzilla 1** released. <ul><li>Released with **Zot**, **OStatus**, and **Diaspora** protocols.</li></ul>                                                                                                                                     |
| 2015        | Planned/added features: articles, cards, wikis, webpages, CalDAV calendar, CardDAV addressbook.                                                                                                                                                |
| Early 2015  | <img src="https://hubzilla.org/cloud/info/website_images_small/hz-16.png" alt="Hubzilla logo" class="me-1"> Renamed from Red Matrix to **Hubzilla**.                                                                                           |
| Early 2015  | Mike Macgirvin stepped down as coordinator; Mario Vavti became Head Developer.<sup>5</sup>                                                                                                                                                     |
| 2015        | Implemented **dynamic groups** (e.g., post to specific demographics or protocols).                                                                                                                                                             |
| 2014        | **Browser-to-browser encryption** introduced; E2EE framework completed.                                                                                                                                                                        |
| 2013        | <img src="https://hubzilla.org/cloud/info/historical_images/red/rm-16.png" alt="Red Matrix logo" class="me-1"> Renamed from Red to **Red Matrix**.                                                                                             |
| 2013        | Turned file storage into access-controlled **WebDAV** nodes for private media uploads.                                                                                                                                                         |
| July 2012   | Created **Zot Protocol** for encrypted fediverse communications and **Nomadic Identity**.                                                                                                                                                      |
| July 2012   | <img src="https://hubzilla.org/cloud/info/historical_images/red/red-16.png" alt="Red logo" class="me-1"> Work began on **Red**, a fork of Free Friendika.<sup>2,3</sup> Mike Macgirvin left Friendica.                                         |
| 25 May 2012 | _The term “fediverse” coined by Mark Eckenwiler._<sup>1</sup>                                                                                                                                                                                  |
| 2012        | Federated WordPress with the fediverse (posts/comments in both directions).                                                                                                                                                                    |
| 12 Nov 2011 | <img src="https://hubzilla.org/cloud/info/historical_images/friendica/friendika-32.png" alt="Friendica logo" class="me-1"> Friendika renamed to **Friendica**.                                                                                 |
| 2011        | **Free Friendika** created; Friendika split into MIT and AGPL versions.<sup>2,3</sup>                                                                                                                                                          |
| 2011        | Began work on **Nomadic Identity** after network shutdowns highlighted migration needs.                                                                                                                                                        |
| 2011        | Brought Facebook and Twitter into the fediverse.                                                                                                                                                                                               |
| 19 Mar 2011 | Added **Diaspora** Federation protocol support.                                                                                                                                                                                                |
| 3 Nov 2010  | <img src="https://hubzilla.org/cloud/info/historical_images/friendica/ff-16.jpg" alt="Friendica logo" class="me-1"> Renamed from Mistpark to **Friendika**.                                                                                    |
| 12 Oct 2010 | Added **OStatus** protocol federation.                                                                                                                                                                                                         |
| 9 Sep 2010  | Added **OpenMicroBlogging** protocol federation.                                                                                                                                                                                               |
| 2010-2011   | Federated with **RSS**, **email**, **Diaspora**, **StatusNet**, and open providers via plugins.                                                                                                                                                |
| 2010        | Provided **access-controlled assets/services**, including media.                                                                                                                                                                               |
| 2010        | Created **federated single sign-on** for decentralized access control.                                                                                                                                                                         |
| 2010        | Introduced **circles/aspects**, **quoted posts**, **comment controls**, **directory services**, **permission/consent**, **DMs**, and **groups** to the fediverse.                                                                              |
| 17 Aug 2010 | Added **DFRN** protocol federation.                                                                                                                                                                                                            |
| 2 Jul 2010  | Launched as **Mistpark**.                                                                                                                                                                                                                      |
| 14 May 2010 | Mike Macgirvin began work on a federated social media server.                                                                                                                                                                                  |

## How to use this documentation?

This guide is organized into several key sections to meet your needs:

- User Manual: Learn how to sign up, post, connect with others, and use Hubzilla’s features. Perfect for newcomers and everyday users.
- Admin Manual: Manage your hub with instructions on setup, moderation, and maintenance. For hub administrators.
- Developer Manual: Extend or customize Hubzilla with code-level insights. For developers and tech enthusiasts.
- API Section: Interact with Utsukta Hub programmatically via our API. For developers building integrations or tools.
- About Utsukta Hub: Discover our hub’s mission, policies, rules, and how to get involved.
- Appendices: Extra resources like glossaries and external links.

Use the navigation bar at the top or the sidebar to jump to any section. Can’t find what you need? Try the search bar or reach out via [email](mailto:admin@utsukta.org).

## Quick Start

- New User? Start with [Getting Started](./user/start.md) in the User Manual.
- Admin? Check out Installation and Setup in the [Admin Manual](./admin/install.md).
- Developer? Dive into the Development Environment or [API Introduction](./api/intro.md).
- Curious about us? Visit [About Utsukta Hub](./about/intro.md).

## Get Involved

Join our community, share your feedback, [contribute](./contribute.md) to this documentation or report an issue via our support forum at [https://hub.utsukta.org/channel/admin] or email us at [support@utsukta.org](mailto:support@utsukta.org). We’re excited to have you here!
