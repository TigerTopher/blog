+++
title = "Tech Blog Speed Run: Hugo and AWS Amplify"
date = "2021-02-18"
cover = "img/2020-02-18-hugo-aws-amplify.png"
description = "Publish your Tech Blog in under 28:59 minutes or less with Hugo and AWS Amplify."
+++

Hey there, humans!

This will be the first tutorial in my blog, and it is all about how this blog has been setup.

The format for this tutorial will resemble that of an RPG wherein we will focus on smashing through the main quests to finish the game. However, there is a catch: we are doing a speedrun to set up our tech blog.

For non-gamers, a speedrun 🏃‍♂️is:

> a play-through, or a recording thereof, of a whole video game or a selected part of it, performed with the intention of completing it as fast as possible.

There are two main reasons why I thought of using this format:

1. Speedrun will minimise the time of setup and remove all the blockers that slows us down from plunging straight to writing content! 👨‍💻
2. Tutorials can be a bit boring so completing one quest after another should make it more doable and rewarding.

## What will you learn? 🤔

Although this will be quick, you will certainly be picking up a thing or two as we go. Topics include:

- Hosting blog site in Github
- Using Static-site generators
- CI/CD: Writing basic pipeline scripts
- Setting up a domain using Route53

## Prerequisites

Here is a list of prerequisites so that the tutorial would be as seamless as possible:

- [Github account](https://git-scm.com/book/en/v2/GitHub-Account-Setup-and-Configuration)
- [AWS account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/)
- [Undivided attention](https://www.youtube.com/watch?v=hP5TNI_2VRs)

Before we finally begin, let me set some expections. Since a lot of materials have already been written online on topics such as setting a Github repo, using Hugo, and deploying in Amplify, I will be referencing other tutorials here. However, this blog should guide you on how to roll all of these tools into one sushi - your tech blog. 🍣

## Main Quests

Starting with an end in mind, let us define our main quests to complete this speedrun:

1. Create blog using Hugo framework and push it to Github
2. Setup Amplify app in AWS and connect it to our Github project
3. Register a domain and connect it to our AWS Amplify App

These quests might be daunting at first glance, but it's really not. 💪 Time is ticking so let's start! ⏱

---

### 📜 Quest #1: Create Hugo Project in Github

Similar to an RPG game, you will be having side-quests for each of our main quests.

Side-quests:

1. Create Github repository
2. Install Hugo
3. Setup Hugo Project
4. Pick Hugo Theme
5. Push changes to Github

---

#### ⚔️ Create Github repository

We will be using [Github](https://github.com/) to host our code. If this is your first time, you can follow this [guide](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-new-repository) to setup your repo. Feel free to name it anything your want, or you can stay classy and name it `blog`. Also, it doesn't matter if the repo is private or public. You should have something like this:

![Github Screenshot](/img/2020-02-18-github.png)

---

#### ⚔️ Install Hugo

💬 What is Hugo?

Hugo's official [site](https://gohugo.io/about/what-is-hugo/) defines it as a fast and modern static site generator written in Go, and designed to make website creation fun again.

💬 What is a Static Site Generator?

SitePoint defines it as:

> A compromise between using a hand-coded static site and a full CMS. You generate an HTML-only website using raw data (such as Markdown files) and templates. The resulting build is transferred to your live server."

💬 Why did I choose to use a Static Site Generator? Few reasons:

- I don't want to deal the hassle of setting up a full CMS in an EC2 server to host a simple blog site like this. There isn't much computation needed and I won't be needing a dynamic database too. However, I don't want to manage HTMLs and CSS too. Best I can do is work with Markdown 😅
- Writing my blog in Markdown using an editor I love sounds more fun than having to write to some generic blog editor. I use this editor everyday, be it at work or leisure coding, so why not for my blog too?
- Hugo has tons of elegant templates I could easily choose from. As you already know, I'm a Security Engineer and CSS and Designing aren't my strongest suite.

Hugo mentions this as the benefit for using Static Site Generators:

> Unlike systems that dynamically build a page with each visitor request, Hugo builds pages when you create or update your content. Since websites are viewed far more often than they are edited, Hugo is designed to provide an optimal viewing experience for your website’s end users and an ideal writing experience for website authors. (Hugo)

If you want to read more, check out: [Benefits of Static Site Generators](https://gohugo.io/about/benefits/).

Now, if you are still here, you probably have been convinced to give Hugo a try. To install Hugo, simply follow this: [Installing Hugo](https://gohugo.io/getting-started/installing/).

---

#### ⚔️ Setup Hugo Project and ⚔️ Selecting a theme

Clone the Github repo that you made and go inside that directory. Example:

```lang=bash
$ git clone git@github.com:<your-username>/blog.git
Cloning into 'blog'...
warning: You appear to have cloned an empty repository.
$ cd blog
```

Next step is to setup Hugo project inside our directory. Luckily, Hugo has this concise quick start guide to cover this: [Quick Start](https://gohugo.io/getting-started/quick-start/).

This tutorial will also cover adding a Hugo theme for your blog. You can find amazing themes in [Hugo Themes](https://themes.gohugo.io/.)

As the time of writing, I went for [hello-friend](https://themes.gohugo.io/hugo-theme-hello-friend/) theme. I love it because it's minimal and has dark-mode.
![Github Screenshot](/img/2020-02-18-hello-friend.png)

If you followed the guide correctly, you should be able to start your server using:

```lang=bash
$ hugo server -D
```

Navigate to your new site at http://localhost:1313/.

If you are satisfied with your setup, feel free to commit your work and do a `git push`.

---

### 📜 Quest #2: Setup AWS Amplify

Coming soon.

<!--
#### AWS Amplify

> AWS Amplify is a combination of client library, CLI toolchain, and a Console for continuous deployment and hosting. The Amplify CLI and library allow developers to get up & running with full-stack cloud-powered applications with features like authentication, storage, serverless GraphQL or REST APIs, analytics, Lambda functions, & more. The Amplify Console provides continuous deployment and hosting for modern web apps (single page apps and static site generators). Continuous deployment allows developers to deploy updates to their web app on every code commit to their Git repository. Hosting includes features such as globally available CDNs, easy custom domain setup + HTTPS, feature branch deployments, and password protection.

Hugo was kind enough to provide us with a guide to setup Hugo for AWS Amplify too: [Hosting on AWS Amplify](https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/).

In the guide
What is a CI/CD Pipeline?

> ...

You can also commit your pipeline file in the root of your repository and name it `amplify.yml`. For my setup, I needed to install certain NPM package to setup.

> What's a pipeline yml.

Once you finish the guide, you should now have a link an amplify link to your app such as https://master.unique-id.amplifyapp.com.

Next step here will be to register our own domain. -->

---

### 📜 Quest #3: Register Domain in Route53

Coming soon.

<!--
What is Route 53?
Guide: https://docs.aws.amazon.com/amplify/latest/userguide/custom-domains.html -->

---

### 🐷 Boss Battle: Share your blog!

Coming soon.

<!-- 🥓Done! -->
