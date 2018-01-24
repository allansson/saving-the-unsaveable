# Saving the unsaveable
How to survive the rewrite without losing all hope

---

## My experience

- Worked at 4 widely different companies
- Youngest codebase 6+ years                                |
- Weirdly similar problems                                  |
- Efforts of lots of well meaning developers over the years |

Note:

---

## Life of a system

+++

### 1994

_Pre-web desktop client_

<!-- .slide: data-background-transition="none" -->
![System architecture](assets/system_arch/15.png)

Note:
Just a thin client directly over a database.

+++
### 1999

_Web portal in ASP and VB6_

![System architecture](assets/system_arch/14.png)

Note:
Web is not useful enough to do everything the desktop client does.

+++

### 2000

_Integrate with 3rd parties by using file exports_

<!-- .slide: data-background-transition="none" -->
![System architecture](assets/system_arch/13.png)

Note:
Mixture of VBScript and scheduled tasks

+++
### 2002

_Rewrite web portal using ASP.NET and WebForms_

<!-- .slide: data-background-transition="none" -->
![System architecture](assets/system_arch/12.png)

Note:
Still using VB though
Some clients remain due to very specific features
Web is pretending it can be useful enough

+++
### 2004

_We need more reports!_

<!-- .slide: data-background-transition="none" -->
![System architecture](assets/system_arch/11.png)

Note:
SSRS and SSAS are added along with a Data Warehouse-database (a.k.a. the cube)
Somewhere, somehow a job is running each night to build "the cube"

+++
### 2005

_File integrations are upgraded to SSIS_

<!-- .slide: data-background-transition="none" -->
![System architecture](assets/system_arch/10.png)

Note:
Not all jobs are migrated

+++
### 2005

_There are whispers of something called SOAP_

<!-- .slide: data-background-transition="none" -->
![System architecture](assets/system_arch/10.png)

Note:
First mentions of a rewrite

+++
### 2007

_Rewrite of web portal in ASP.NET MVC_

<!-- .slide: data-background-transition="none" -->
![System architecture](assets/system_arch/09.png)

Note:
90% of UI is just the old portal in an iframe
Sold to a bunch of customers as Next Generation

+++
### 2009

_Source Control is invented!_

![System architecture](assets/system_arch/09.png)

Note:

+++
### 2010

_Yet another rewrite of web portal in MVC is started_

![System architecture](assets/system_arch/08.png)

Note:

+++
### 2011

_We need to use SOA!_

![System architecture](assets/system_arch/07.png)

Note:
A new database is created
New API is just a thin wrapper over the new database
Some attempts to re-use in desktop client

+++
### Late 2012

_New web portal is relased_

![System architecture](assets/system_arch/07.png)

Note:
Only 40% completed

+++
### Christmas 2012

_Discovered new portal messes up statistics_

![System architecture](assets/system_arch/06.png)

Note:
A new database sync agent is created to sync data from the new database to the old

+++
### Spring 2013

_Customers complain data updated in old portal is not visible in new portal_

![System architecture](assets/system_arch/05.png)

Note:
The sync agent is updated to also sync data from the old database to the new

+++
### Spring 2013 + 1 weeks

_Database gets corrupted due to old data being synced is synced back again_

![System architecture](assets/system_arch/04.png)

Note:
Database backup restored. One week of customer data lost.
Sync job is fixed
The code is a nightmare
This will become a scar in the organization

+++
### Spring 2013 + 2 weeks

_Management bans "rewrite" from corporate dictionary_

![System architecture](assets/system_arch/03.png)

Note:
Executive decision is that migrating from old database is not an option


+++
### Spring 2013 + 3 weeks

_Developers start talking about refactoring_

![System architecture](assets/system_arch/03.png)

Note:

+++
### 2015

_JSFotM-movement has gained momentum_

![System architecture](assets/system_arch/02.png)

Note:
JavaScript Framework of the Month
Grunt, Gulp, Webpack
jQuery-Knockout-Angular-React

+++
### 2016

_We need to be Microservice-compliant_

![System architecture](assets/system_arch/01.png)

Note:
Changing the database is still too much. Single integration database.

+++
### 2018

_You are hired to clean up this mess!_

![System architecture](assets/system_arch/01.png)

Note:

---
## What can a poor developer do?

- Toxic sentiments |
  - "We'll rewrite this code soon anyway" |
  - "This code is s**t anyway, just do a dirty hack" |
  - "Easier to rewrite it all" |

+++
## What can a poor developer do?

> The only thing necessary for the triumph of evil is for good men to do nothing.
>
> _Edmund Burke_

---
## The rewrite fallacy

> "It would be easier to rewrite the entire thing than to continue working
> with the code as it is today"

+++
## The rewrite fallacy

> If you think you understand quantum mechanics, then you don't understand quantum mechanics.
>
> _Richard Feynman_

> The only true wisdom is knowing you know nothing.
>
> _Socrates_

## The rewrite fallacy

- Software accumulates knowledge over time |
- All those quirks mattered at some point |
- Odds are nobody remembers why |

---
## The rewrite pitfall

- The rewrite is granted!
- Developers rejoice! |
- New git repository created |
- The hacking starts

+++
## The rewrite pitfall

18 months of work. Implemented the exact same system, but used REST instead of SOAP.

---
## Avoiding the pitfall

- 
- Question your own knowledge
  - how you write code
  - how your business operates         |