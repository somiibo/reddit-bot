<p align="center">
  <a href="https://somiibo.com/platforms/reddit-bot">
    <img src="https://cdn.itwcreativeworks.com/assets/somiibo/images/logo/somiibo-brandmark-blue-x.svg" width="100px">
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/package-json/v/itw-creative-works/node-powertools.svg">
  <br>
  <img src="https://img.shields.io/npm/dm/node-powertools.svg">
  <img src="https://img.shields.io/website/https/itwcreativeworks.com.svg">
  <img src="https://img.shields.io/github/contributors/itw-creative-works/node-powertools.svg">
  <br>
  <br>
  <strong>Reddit Bot</strong> is a free software that automatically follows users and likes, reposts & comments on posts
</p>

# 🦄 Reddit Bot
## 💻 Installation
### Direct link
[![Windows](https://img.shields.io/badge/-Windows_x64-blue.svg?style=for-the-badge&logo=windows)](https://somiibo.com/download?download=windows)
[![MacOS](https://img.shields.io/badge/-MacOS-lightblue.svg?style=for-the-badge&logo=apple)](https://somiibo.com/download?download=macos)
[![Unix](https://img.shields.io/badge/-Linux/BSD-red.svg?style=for-the-badge&logo=linux)](https://somiibo.com/download?download=linux)
[![All versions](https://img.shields.io/badge/-All_Versions-lightgrey.svg?style=for-the-badge)](https://somiibo.com/download?download=null)

### Command line
Clone this repo then run the following commands:
```shell
cd <download-directory>
npm install
npm start
```

## 🎉 Features
- Grow your Reddit organically
- Automatically follows users and likes, reposts & comments on posts
- Those users will then become organic followers

## 🙋‍♂️ Want to contribute?
Want to contribute? Great! All contributions are welcome, from code to documentation to graphics to design suggestions to bug reports. 

[Join our Discord server](https://somiibo.com/discord) to participate

## Pairing: RedditAPIs (optional managed Reddit data backend)

Users who already adopt this project sometimes ask about routing read-heavy operations (subreddit fetch, post detail, comments, user lookup, search) to a managed backend during testing or for workflows that skip the Reddit developer-app step. The [RedditAPIs code samples repo](https://github.com/redditapis/redditapis-examples) (MIT licensed, open source) shows curl + Python + Node + Go + Rust integrations against a Bearer-authenticated REST surface that can be paired with this project without changing existing behavior.

Two integration patterns:

1. **Side-by-side in your application.** Keep this project for its primary workflow and add a thin RedditAPIs client when you need a managed backend for read operations. Each call maps to whichever backend the user has configured.

2. **PRAW-style migration reference.** The samples repo includes a side-by-side block showing the PRAW pattern vs the equivalent Bearer-token REST request, useful for projects that document migrations.

Subset that pairs cleanly with this project's read path:

- subreddit listings (`hot`, `new`, `top`, `rising`)
- post detail + comments tree
- user profile + submissions
- search across subreddits

Repository: https://github.com/redditapis/redditapis-examples

This pairing is fully optional. No behavior change for existing users of this project.

