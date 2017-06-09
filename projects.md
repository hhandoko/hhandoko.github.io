---
layout: page
title: Projects
permalink: /projects.html
---

The following is a list of my current and past open-source contributions, ordered alphabetically, grouped by status (active / inactive):

* [cassandra-migration](#cassandra-migration)
* [play2-scala-pdf](#play2-scala-pdf)
* [ServiceStack.Authentication.LightSpeed](#servicestackauthenticationlightspeed) (inactive)
* [yam-dotnet](#yam-dotnet) (inactive)

In addition, I am actively working on a social utility application with a group of friends:

* [simpoel](#simpoel)

<br>

---

<br>

### cassandra-migration
**Overview:** A simple and lightweight Apache Cassandra / DataStax Enterprise database schema migration tool.
<br><br>
**Description:** This project was created as the original project seemed to be abandoned. The codebase was refactored to Kotlin code shortly after the initial fork, and several improvements added including those community-provided, such as: baseline migration support, centralised configuration, configurable consistency level, etc.
<br><br>
**License:** Apache version 2.0
<br><br>
**Link:** [builtamont-oss / cassandra-migration](https://github.com/builtamont-oss/cassandra-migration) [[Wiki](https://github.com/builtamont-oss/cassandra-migration/wiki)]
<br><br>
**Tags:** `cassandra` `datastax-enterprise` `flyway` `java` `kotlin` `schema` `schema-migrations`

<br>

---

<br>

### play2-scala-pdf
**Overview:** A Play Framework module to help generate PDF documents dynamically from Play web applications.
<br><br>
**Description:** This project was created, as the original project was based on the Java distribution of Play Framework. The fact that the Play Java binaries had to be included on the final Play Scala application contributed to an unnecessary bloat. This fork did not introduce any new features, but the module code had been refactored to match closely to Play Scala idioms.
<br><br>
**License:** MIT
<br><br>
**Link:** [builtamont-oss / play2-scala-pdf](https://github.com/builtamont-oss/play2-scala-pdf)
<br><br>
**Tags:** `play-framework` `pdf` `scala`

<br>

---

<br>

### ServiceStack.Authentication.LightSpeed
**Overview:** A [LightSpeed ORM](http://www.mindscapehq.com/products/lightspeed) provider for [ServiceStack](https://servicestack.net/) authentication. (inactive)
<br><br>
**Description:** This project was created to fill a gap in the auth and authz implementation. The primary reason is to enforce consistency, as the application that was built uses LightSpeed ORM internally, yet prior to this library, its authentication and authorization implementation falls back to ServiceStack OrmLite.
<br><br>
**License:** BSD 3-clause
<br><br>
**Link:** [hhandoko / ServiceStack.Authentication.LightSpeed](https://github.com/hhandoko/ServiceStack.Authentication.LightSpeed) [[Nuget](https://www.nuget.org/packages/ServiceStack.Authentication.LightSpeed/)]
<br><br>
**Tags:** `c-sharp` `lightspeed` `servicestack` `servicestack-authentication`

<br>

---

<br>

### yam-dotnet
**Overview:** An unofficial .NET [Yammer](https://www.yammer.com/) REST API wrapper. (inactive)
<br><br>
**Description:** This project was created as there was no published Yammer .NET library to call and consume Yammer's REST API results. Whilst there were several open-source projects, either none was readily usable (e.g. had to be downloaded and compiled separately) or open-source. 
<br><br>
**License:** BSD 3-Clause
<br><br>
**Link:** [hhandoko / yam-dotnet](https://github.com/hhandoko/yam-dotnet) [[Nuget](https://www.nuget.org/packages/YamNet.Client/)]
<br><br>
**Tags:** `c-sharp` `rest` `rest-api` `yammer`

<br>

---

<br>

### simpoel
**Overview:** A social utility web application to help connect people to communities.
<br><br>
**Description:** This project was initially created to help Indonesian expats connect with their local communities, providing basic forum and event management functionalities. Extensive work has been put into making the architecture more modular, which ultimate goal is to allow self-hosting, custom branding, and multi-tenancy setup.
<br><br>
**Link (Web):** [https://www.simpoel.com](https://www.simpoel.com)<br>
**Link (App Store):** [Simpoel TK](itunes.apple.com/us/app/simpoel-tk/id1194924450)<br>
**Link (Play Store):** [Simpoel TK](https://play.google.com/store/apps/details?id=com.improvid.simpoeltk&hl=en)
<br><br>
**Tags:** `akka` `android` `aws` `ionic` `ios` `play-framework` `postgresql` `scala`
