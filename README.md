# v.1.0
OhmJet website powered by Hugo
<img width="1264" alt="screenshot" src="https://github.com/user-attachments/assets/9b9bf4fc-8644-42d7-baed-c71184f468f5">

# Intro

The main reason we decided to publish this repo is that we want to show you how simple it is to build your website from scratch without technical knowledge.

The main goal for site was to create if from scratch and host it for free.  You can see here all steps from domain registration to static files hosting. 

# About HUGO 

For our own website https://ohmjet.com our team choosen HUGO as a main framework and here couple reason why: 

1. Price. It is free
2. Google site speed result. It is faster than outher frameworks.
3. Technical knowleges. It doesn't need any technical skills. The first steps were done without needing to write code.
4. Time to market. As usual it takes a lot of time to develop site from the scratch. In a case of Hugo it took not more than 1 day from domain registration to hosting your files
5. Massive developers community. As next plan after design the final UI/UX for website we plan work with developers from community and don't plan to have our own.
6. SEO. It has a lot of components and facilities to be optimized for organic marketing. 

In sum we belief that HUGO is the fastest and professional pathway to have rapidly fast , beutiful and SEO optimized website. 

# About Clouflare 

Before starting this projesct we were not fimilar with CloudFlare pages. So for planty of developers it might be xtrange but we have never user CF for hosting. And when we tried it with HUGO it was amazing experience. 
In couple clicks and terminal commands you are able to have hosted site arount 10 min. 

Let's speak about CloudFlare pages. The majour reasons why we choosen it : 

1. Fastest network: run your site on the Cloudflare edge, milliseconds from end users – up to 115% faster than competing platforms.
2. Incredibly scalable: with one of the world’s largest networks, Cloudflare can absorb traffic from the most visited sites.
3. Always secure: SSL works out of the box, so you never have to worry about provisioning certificates.
4. Stay ahead of the curve: support for the latest web standards with HTTP/3, QUIC, image compression out of the box, and more.

In addition we have had good experience with deploynebt and with ths servicing of project. SSL is available by default . Everything that you need is direct your domain to CloudFlare ( In our case the domain provider is Godaddy) 

# About Godaddy 

As usual for domain registration our team ueses Goddady. Godaddy is the bigest one provider with the a lot of discount. 
We registered our own domain https://ohmjet.com for 5$ and as you know each website starts from domain name. 
It could be the first step in a buisness establishing. For us it works. Everytime when we start buisness from Brand Name, so your domain, as usual, is equal to the business name.


# Step-by-step guide How to launch your website 

1. Find and register doamin name that fits your brand. In our case it is ohmjet.com . 
a) Follow to https://www.godaddy.com/
b) Create account
c) Purchuse your domain and be happy.

2. Find out Hugo ducumentation by following this link https://gohugo.io/documentation/ 
We want to save your time and share with steps that were work for us :

Ex. for MacOS 
a) You should install brew if you don't have it. Please use this link and be ready https://brew.sh/ Homebrew is a free and open-source package manager for macOS and Linux. 
b) To install the extended edition of Hugo Use this SSH comand.

```
brew install hugo

```
c) Verify that you have installed Hugo v0.112.0 or later.

```
hugo version

```
b) Run these commands to create a Hugo site . The next section provides an explanation of each command.  

```
hugo new site quickstart

```
quickstaet it the name of your project (website). In our case it is OhmJet


c) Follow to your site folder 

```
cd quickstart

```

d) Install your theme. In our case it was "hugo-serif-theme" . And at first we did mistake and we didn't fork it. Our suggestion if you need to make changes in theme such as add cookies manager or anything else you should frork theme at first and only after that deploy it from your repository.

You should have git https://git-scm.com/  installed before follow next steps 

```
git init

git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke

echo "theme = 'ananke'" >> hugo.toml

```
For out project we use this template https://www.zerostatic.io/theme/hugo-serif/  . It is totally free and Open Source. So you can choose it.  But in command example we used Ananke theme.


e) Run Hugo project on your local machine


```
hugo server

```

That is it for HUGO local machime setup. 

3. For hosting we have used ClouFlare. We have choice between Github Pages and CloudFlare pages but CloudFlare works better for us. Because CF could cover everything that related security (SSL , Firewall) and analytic.
You can compare Github pages and CF pages by following links : 

https://pages.cloudflare.com/ 
https://pages.github.com/ 

To deploy your site to Pages: 

a) Log in to the Cloudflare dashboard and select your account.
b) In Account Home, select Workers & Pages > Create application > Pages > Connect to Git.
c) Select the new GitHub repository that you created and, in the Set up builds and deployments section, provide the following information: 

Production branch - 	main
Build command	- hugo
Build directory	- public

Base URL configuration
Hugo allows you to configure the baseURL of your application. This allows you to utilize the absURL helper to construct full canonical URLs. In order to do this with Pages, you must provide the -b or --baseURL flags with the CF_PAGES_URL environment variable to your hugo build command.

Your final build command may look like this:

```
hugo -b $CF_PAGES_URL
```

d) After completing deployment configuration, select the Save and Deploy. You should see Cloudflare Pages installing hugo and your project dependencies, and building your site, before deploying it.
   
Congrats that is it. After deploying your site, you will receive a unique subdomain for your project on *.pages.dev. Every time you commit new code to your Hugo site, Cloudflare Pages will automatically rebuild your project and deploy it. You will also get access to preview deployments on new pull requests, so you can preview how changes look to your site before deploying them to production.


# How to edit your Hugo site and deploy updates to CF pages and github 

For files editiong we use Sublime Text https://www.sublimetext.com/   You can use aby other code/text editers but we love this one. 

For send updates to server the most workable command list for us : 

```
git add .
git commit -m "test"
git pull --rebase origin main
git push origin main

```


















