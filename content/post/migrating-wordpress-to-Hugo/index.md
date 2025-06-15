---
title: How I migrated from Wordpress to Hugo and saved hundreds of dollars
date: 2025-06-15
categories:
  - budget
tags:
  - saving
  - minimalism
---
## Background

I started [happypathFire](https://happypathfire.com/) in 2019 as an attempt to share my thoughts on FIRE (Financial Independence Retire Early). At the time, I just started writing blogs and had never built a public facing website. I had used platforms like Medium and blogger before but I wanted something more personal and something that is more independent and is not subject to the arbitrary content policies of the companies behind those platforms. 

### Why Wordpress?

I chose Wordpress for its ease of use and the availability of a huge market of free plugins to solve almost all of my needs. In addition to this, Wordpress is available pre-installed in most hosting providers. 

### Bluehost

To be honest, the reason I chose bluehost as a hosting provider is due to [gocurrycracker.com](https://www.gocurrycracker.com/). 
I benefitted a lot from Jeremy and his really inspiring blog posts. Jeremy had an affiliate link to bluehost and I thought it is a reasonable way to show my support to his work. 

From 2019 to 2025, I have used the services of bluehost and the support team was quite excellent to resolve my issues. Things were going great!

## Why change now?

## Principles

As any follower of the FIRE movement would know, the core principles of FIRE is to be constantly on top of expenses and find innovative ways to reduce them without compromising on quality of life. I found that the hosting costs at bluehost were adding up and I wanted to look for a better, less expensive option.

> Loyalty is a punishable offence !!!

### Bait and Hike

Bluehost offers generous pricing when someone signs up to the their services. But, as time goes on they consistently hike prices. Back when I started my annual hosting costs were 30$s. However, I noticed at every renewal of my subscription the price kept going up. The quote I got for 2025 was 200$s per year including taxes!!!

This was getting a bit out of hand. A quick math check on the cost of maintaining the website over a period of 10 years would run into the thousands. That too not accounting for any future increases, which is almost a certainty. 

### Sustainability

The final and perhaps the stronger motivation to look for alternatives was sustainability. If something were to happen to me the website would cease to exist because bluehost would shut down my website if it did not receive payments in time.

I needed a solution that was more sustainable

## Hugo + Github pages

In my search for alternatives I looked at various alternatives and landed on Hugo and Github pages.
[Hugo](https://gohugo.io/) is an open-source static website building framework and is a delight to use. It is fast and easy to adapt. Github pages provides hosting for the web-content.

Here is how I went about migrating. Note that this is not a comprehensive guide but a high-level overview of the steps involved. For a detailed guide use any of the LLMs(Large Language Models) like Claude, Chatgpt etc.

#### Step 1 : Export Wordpress site content
You can export your wordpress site by logging into your wordpress admin dashboard on bluehost and using the tools. Pro tip: change any custom theme that you might have into a native wordpress theme. This will be useful in the conversion step where you will have less stuff to clean-up

#### Step 2 : Backup images
If your wordpress website uses images like mine does, make sure you backup those images. This can be done by logging into settings-> File manager . (this is accessed from Bluehost admin and not from your wordpress admin)

#### Step 3 : Setup Github account

#### Step 4 : Install Hugo

#### Step 5 : Convert wordpress to Markdown
This is the most important step. You need to convert your wordpress file that you exported from Step 1 into markdown format. Hugo relies on the markdown format. It is the format in which you will be able to create/edit your posts going forward. It is simple and easy to learn and has a very small learning curve.
There are several solutions to convert wordpress to markdown including some on the web. I found *wordpress-export-to-markdown* to work best. It not only converted the text to markdown but also downloaded the images on each of the posts and neatly organised them into folders that Hugo could access. 
The exact command that worked for me was
```
npx wordpress-export-to-markdown --wizard false --input ~/my-file-exported-from-wordpress.xml --output ~/some-temp-folder-to-save-output
```

#### Step 6 : Copy converted content into the location you installed Hugo

#### Step 7 : Select theme and configure Hugo
There are a lot of open-source themes available for Hugo and they are curated well on the [Hugo website](https://themes.gohugo.io/). 

#### Step 8 : Test locally and fix any issues
Be prepared to be amazed at how fast Hugo is able to generate your website. The live-reload on any edits you make are lightning fast!

#### Step 9 : Push to Github
Create a public repository on Github for your website and push your code to it.

#### Step 10 : Create Github actions to auto-build your site and Re-point your DNS
Github actions builds your website for you as soon as you make changes or add new posts and push the code to your Github repo.
Note that if your DNS is also on bluehost you have 2 options. You can continue to use bluehost for your Domain name services or you could move to some other provider. I had made the move out of bluehost DNS previously as I noticed they were hiking those prices too.

#### Adding new posts
Whenever you want to edit/add posts. You can use any markdown editor for this purpose. Make your changes locally and push it to Github and you are done!
I use Obsidian for this purpose. The biggest benefit of using obsidian is that it looks-up the categories and tags for me automatically as I create new posts. This is extremely useful to make your website content-rich and keep it functionally similar to wordpress.

Overall these steps may appear daunting but trust me, using the support of LLMs you will be able to make this migration quite easily. 
## Conclusion

With the above changes, my annual costs went down from about 200$s to 10$s (10$s is the annual cost of DNS only)
It may look like a case of *much ado about nothing* but it is not really about the cost. It is about principles. Recurring costs like subscriptions are something one has to pay really close attention to. They may seem like a small amount but they are in-fact a clever strategy marketers use to trick our mind to pay more over time. Staying on top of such *trifles* is how you stay on the path of FIRE!!! 





