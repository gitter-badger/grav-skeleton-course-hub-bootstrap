# Course Hub Bootstrap Skeleton (unreleased)

The **Course Hub** skeleton is intended to accompany a face-to-face, blended or fully online university course. It supports a [flipped-LMS approach](http://hibbittsdesign.org/blog/posts/flipped-lms-using-an-open-and-collaborative-platform) using the modern flat-file (no database) Grav CMS as an open and collaborative Web platform.

**Table of Contents**  
[Why Flip your LMS with Grav?](#why-flip-your-lms-with-grav)  
[Why Use a Modern flat-file CMS?](#why-use-a-modern-flat-file-cms)  
[Course Hub Bootstrap Screenshot](#course-hub-bootstrap-screenshot)  
[Course Hub Highlights](#course-hub-highlights)  
[Quick Install (Web server only)](#quick-install-web-server-only)  
[Recommended Install (Desktop + Server)](#recommended-install-desktop--server)  
[Page Templates](#page-templates)  
[Site Structure](#site-structure)
[Configuration](#site-configuration)  

## Why Flip your LMS with Grav?
* To support pedagogical goals unmet by current LMS/platform
* To increase capability of access, sharing and collaboration
* To deliver a better student (and facilitator) experience

## Why Use a Modern flat-file CMS?
As an open source modern flat-file CMS, Grav offers a distinct set of advantages to Web-savvy educators looking to move beyond their institutional LMS:
* Modern means...
  * Modern PHP code (i.e. reliability, speed, extensibility, etc.)
  * Use of current standards (i.e. Markdown, Twig, YAML, etc.)
  * Modular/customizable content chunks (i.e. reuse of content)
  * Further separation of content (i.e. files) from presentation
* Flat-file means...
  * No database means less (or no) IT involvement needed
  * Content stored in text files rather than in a database
  * Takes full advantage of the collaborative ecosystem now available (i.e. GitHub)
  * Increased portability, as moving a site now only requires simply copying files to another location
  * All template and content files are 100% version controllable

## Course Hub Bootstrap Screenshot
![Course Hub Bootstrap Screenshot](/assets/screenshot.jpg)  
_Figure 1. Example Grav Course Hub website, with GitHub collaborative editing enabled and Olark instant chat installed. Explore the demo online at [demo.hibbittsdesign.org/grav-course-hub-bootstrap/](http://demo.hibbittsdesign.org/grav-course-hub-bootstrap/)_

## Course Hub Highlights
* A complete ready-to-run Grav package (open source)
* Blog-format, with important reminders & top sticky post
* Site pages can be easily added/removed/changed
* Image header area above site navbar
* Sidebar is a simple markdown file, which can also contain HTML
* URL flag to only display page content (for display within LMS). For example, [demo.hibbittsdesign.org/grav-course-hub-bootstrap/blog/week-03/onlydisplaypagecontent:true](http://demo.hibbittsdesign.org/grav-course-hub-bootstrap/blog/week-03/onlydisplaypagecontent:true)
* External links are automatically opened in a new Tab/Window
* Built-in support for entire site to be collaboratively maintained on GitHub
* Since everything is built with Grav it can be _entirely_ customized

To learn more about how to most effectively use the Grav Course Hub, visit [hibbittdesign.org](http://hibbittsdesign.org/blog/)

## Quick Install (Web server only)
**Pre-flight Checklist**  

1. Confirm Web server PHP version (PHP 5.5.9 or higher)
2. Web server login credentials (username and password)

**Installation Steps**  

1. Download the ready-to-run [Course Hub Skeleton Package](http://hibbittsdesign.org/blog/downloads/grav-skeleton-course-hub-site.zip)
2. Unzip the package onto your desktop  
3. Copy the entire Grav Course Hub folder to your Web server  
4. Point your browser to the Web server folder  
5. Create your site administrator account when prompted  
6. And you're done! (press the ![Right Arrow Circle Icon](/assets/fa-arrow-circle-right.png) icon in the Admin Panel to preview site)

## Recommended Install (Desktop + Server)
With the flat-file (no database) nature of Grav, there are lots of benefits of installing Grav on your computer and then having your site files mirrored onto a Web server:
* Always have access to your site, regardless of Web server status
* Develop and test changes to your site privately without any downtime of the live site
* Store your site files on a Git service (i.e. GitHub) to better track your development and enable anywhere, anytime editing of your site
* Enable others (i.e. students, fellow instructors, colleagues, etc.) to collaboratively contribute to the site, including both site content _and_ code  

![Grav recommended install using Grav, GitHub, and Deploy to support a flipped-LMS approach](/assets/flipped-lms-grav-github-deploy-2.png)  
_Figure 2. Grav recommended install using Grav, GitHub, and Deploy to support a flipped-LMS approach._

**Pre-flight Checklist**  

1. Confirm Web server PHP version (PHP 5.5.9 or higher)  
2. Web server login credentials (username and password)  
3. Download and install MAMP   ([https://www.mamp.info/](https://www.mamp.info/))  
4. Git server account (e.g. GitHub ([https://github.com/](https://github.com)) or local GitLab or Gogs app, etc.)  
5. Download and install GitHub Desktop ([https://desktop.github.com/](https://desktop.github.com/))  
6. Automatic deployment service (e.g. Deploy ([https://www.deployhq.com/](https://www.deployhq.com/)), FTPploy([https://ftploy.com/](https://ftploy.com/)), etc.)  

**Desktop Installation Steps**  

1. Download the ready-to-run [Course Hub Skeleton Package](http://hibbittsdesign.org/blog/downloads/grav-skeleton-course-hub-site.zip)
2. Unzip the Grav package onto your desktop
3. Create a folder called 'MAMP Websites' in your 'Documents' folder
4. Copy the _entire_ Grav folder into your 'MAMP Websites' folder
5. Launch MAMP
6. Change the 'Document Root' MAMP preferences setting to the 'MAMP Websites' folder (within 'Documents')
7. Press the MAMP 'Start Servers' button
8. Enter 'localhost:8888' as the URL in your Web Browser
9. Choose the displayed Grav folder name
10. Create your site administrator account when prompted
11. And you're done! (press the ![Right Arrow Circle Icon](/assets/fa-arrow-circle-right.png) icon in the Admin Panel to preview site)  

Once you have confirmed that Grav is running locally on your computer, the final step is to create a Git server repository to store your site files and setup an automatic deployment service to push any changed files to your Web server. An example step-by-step walkthrough this process is available in the article [Using Grav with GitHub Desktop (and Deploy)](http://hibbittsdesign.org/blog/posts/using-grav-with-github-and-deploy).

## Page Templates
* Blog template (blog.html.twig)
* Important reminders template (important_reminders.html.twig)
* Weekly preparations template (preparations.html.twig)
* Blog item template (blog_item.html.twig)
* Item template (item.html.twig)
* Page template (page.html.twig)
* Sidebar template (sidebar.html.twig)

## Site Structure
```
/user
  - /pages
    - /01.blog | blog.html.twig and blog_item.html.twig
      -/_important-reminders | important_reminders.html.twig
      -/_preparations | preparations.html.twig
      -/week-01 | item.html.twig
      -/week-02 | item.html.twig
      - etc..
    - /02.resources | page.html.twig
      -/page.md
    - /03.syllabus | page.html.twig
      -/page.md
    - /headerimage | default.html.twig
      -/default.md
```

## Site Configuration

The 'site.yaml' file located in the '/user/config/' folder contains the following default values:
```
title: CPT-363
metadata:
    description: 'A short description of your course would go here'
displaymenuentries:
    enabled: false        # display of additional menu entries
menu:                     # menu entry for adding external sites/tools
    - text: Grav
      icon: arrow-circle-right
      url: http://getgrav.org/
icon:                     # default font awesome icons for preparation and post entries
    posts: calendar-o
github:
    location: none         # menu | page | none
    tree: https://github.com/hibbitts-design/grav-skeleton-course-hub-bootstrap/edit/master/
rssbutton:
    display: true
```

| Setting | Child Setting | Description                                                                                                            |
|---------|---------------|------------------------------------------------------------------------------------------------------------------------|
| title   |               | The course number/id, to be displayed at the top of every page.                                                      |
| metadata  |  description | The short description of the course hub site                                       |
| displaymenuentries  |  enabled | Can be set to `true` or `false`. When set to `true`, all defined menu items are added to the navbar.                                       |
| menu  |  text | Text label for external links to be included on navbar                                       |
| menu  |  icon | Font awesome icon code for external link (optional)                                        |
| menu  |  url | URL for external link|                                    
| icon  | preparations    | Change the default font awesome icon for the preparation area on the home page. |
| icon  | posts          | Change the default font awesome icon for the weekly blog posts (i.e. weekly summaries).           |
| rssbutton  | display       | Can be set to `true` or `false`. When set to `true`, it displays RSS buttons on the sidebar for each page. |
| github  | location       | Can be set to `page`, `menu` or `none`. When set to `page` or `menu`, it will display the **Edit this page** link to your GitHub repo in the indicated location. |
| github  | tree          | Sets the tree by which your site's content is based. Generally the repo your site's content is pulled from.            |

---
