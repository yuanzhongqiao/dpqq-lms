<p align="center">
  <a href="https://www.frappelms.com/">
    <img src="https://frappe.io/files/lms.png" alt="Frappe LMS" width="50px" height="50px">
  </a>
  <p align="center">Easy to use, open source, learning management system.</p>


  <p align="center">易于使用、开源、学习管理系统。</p>
</p>


&nbsp;

<p align="center">
    <a href="https://www.producthunt.com/posts/frappe-lms?utm_source=badge-top-post-topic-badge&utm_medium=badge&utm_souce=badge-frappe&#0045;lms" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-topic-badge.svg?post_id=396079&theme=dark&period=weekly&topic_id=204" alt="Frappe&#0032;LMS - Easy&#0032;to&#0032;use&#0044;&#0032;100&#0037;&#0032;open&#0032;source&#0032;learning&#0032;management&#0032;system | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>
</p>


<div align="center" style="max-height: 40px;">
    <a href="https://frappecloud.com/lms/signup">
        <img src=".github/try-on-f-cloud.svg" height="40">
    </a>
</div>

&nbsp;

<p align="center">
	<a href="https://dashboard.cypress.io/projects/vandxn/runs">
    <img alt="cypress" src="https://img.shields.io/endpoint?url=https://dashboard.cypress.io/badge/simple/vandxn/main&style=flat&logo=cypress">
  </a>
  <a href="https://github.com/frappe/lms/blob/main/LICENSE">
    <img alt="license" src="https://img.shields.io/badge/license-AGPLv3-blue">
  </a>
</p>

<img width="1402" alt="Lesson" src="https://frappelms.com/files/banner.png">

<details>
	<summary>Show more screenshots</summary>
	<img width="1520" alt="ss1" src="https://user-images.githubusercontent.com/31363128/210056046-584bc8aa-d28c-4514-b031-73817012837d.png">
	<img width="830" alt="ss2" src="https://user-images.githubusercontent.com/31363128/210056097-36849182-6db0-43a2-8c62-5333cd2aedf4.png">
	<img width="941" alt="ss3" src="https://user-images.githubusercontent.com/31363128/210056134-01a7c429-1ef4-434e-9d43-128dda35d7e5.png">
</details>


## 介绍

Frappe LMS 是一个易于使用的开源学习管理系统。您可以使用它来创建和共享在线课程。该应用程序具有清晰的 UI，可帮助学生只专注于重要的事情，并有助于无干扰的学习。

您可以通过简单的表单创建课程和课程。课程可以采用文本、视频、测验或所有这些的组合形式。您可以让学生参与测验，以帮助复习和测试所学的概念。课程教师和学生可以通过每节课的讨论部分相互联系，并解决疑问。

## 特征
 创建在线课程。📚

 向课程添加详细说明和预览视频。🎬

 将视频、测验和作业添加到您的课程中，使其有趣且具有互动📝性

 每节课下方的讨论部分，教师和学生可以在其中相互交流。💬

 创建批次以根据课程对学生进行分组并跟踪他们的进度 🏛

 Statistics 仪表板，一目了然地提供所有重要数字。📈

 用户可以在其中发布和查找工作。💼

 包含每个人的个人资料页面👨 👩 👧 👦的 People 目录

 设置封面图片、个人资料照片、简短简历和其他专业信息。🦹🏼‍♀️

 优化可读性🤓的简单布局

 整体使用✨中的愉快用户体验

技术栈

Frappe LMS is an easy-to-use, open-source learning management system. You can use it to create and share online courses. The app has a clear UI that helps students focus only on what's important and assists in distraction-free learning.

You can create courses and lessons through simple forms. Lessons can be in the form of text, videos, quizzes or a combination of all these. You can keep your students engaged with quizzes to help revise and test the concepts learned. Course Instructors and Students can reach out to each other through the discussions section available for each lesson and get queries resolved.

## Features
- Create online courses. 📚
- Add detailed descriptions and preview videos to the course. 🎬
- Add videos, quizzes, and assignments to your lessons and make them interesting and interactive 📝
- Discussions section below each lesson where instructors and students can interact with each other. 💬
- Create batches to group your students based on courses and track their progress 🏛
- Statistics dashboard that provides all important numbers at a glimpse. 📈
- Job Board where users can post and look for jobs. 💼
- People directory with each person's profile page 👨‍👩‍👧‍👦
- Set cover image, profile photo, short bio, and other professional information. 🦹🏼‍♀️
- Simple layout that optimizes readability 🤓
- Delightful user experience in overall usage ✨

## Tech Stack

Frappe LMS is built on [Frappe Framework](https://frappeframework.com) which is a batteries-included python web framework.
These are some of the tools it's built on:
- [Python](https://www.python.org)
- [Redis](https://redis.io/)
- [MariaDB](https://mariadb.org/)
- [Socket.io](https://socket.io/)

## Local Setup

### Docker
You need Docker, docker-compose, and git setup on your machine. Refer to [Docker documentation](https://docs.docker.com/). After that, run the following commands:
```
git clone https://github.com/frappe/lms
cd apps/lms/docker
docker-compose up
```

Wait for some time until the setup script creates a site. After that, you can access `http://localhost:8000` in your browser and the app's login screen should appear.
You'll have to go through the setup wizard to set up the website the first time you access it. Log in using the following credentials to complete the setup wizard.

```
Username: Administrator
password: admin
```

### Frappe Bench

Currently, this app depends on the `develop` branch of [frappe](https://github.com/frappe/frappe).

1. Setup frappe-bench by following [this guide](https://frappeframework.com/docs/v14/user/en/installation)
1. In the frappe-bench directory, run `bench start` and keep it running. Open a new terminal session and cd into the `frappe-bench` directory.
1. Run the following commands:
    ```sh
    bench new-site lms.test
    bench get-app lms
    bench --site lms.test install-app lms
    bench --site lms.test add-to-hosts

 1. Now, you can access the site at `http://lms.test:8000`


## Deployment
Frappe LMS is an app built on top of the Frappe Framework. So, you can follow any deployment guide for hosting a Frappe Framework-based site.

### Managed Hosting
Frappe LMS can be deployed in a few clicks on [Frappe Cloud](https://frappecloud.com/marketplace/apps/lms).

### Self-hosting
If you want to self-host, you can follow official [Frappe Bench Installation](https://github.com/frappe/bench#installation) instructions.

## Bugs and Feature Requests
If you find any bugs or have a feature idea for the app, feel free to report them here on [GitHub Issues](https://github.com/frappe/lms/issues). Make sure you share enough information (app screenshots, browser console screenshots, stack traces, etc) for project maintainers.

## License
Distributed under [GNU AFFERO GENERAL PUBLIC LICENSE](license.txt)
