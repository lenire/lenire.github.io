---
layout: post
title:  "Active Directory Setup"
date: 2021-05-02 -0500
categories: ActiveDirectory
---
Today was a big stop for me. I have spent the past year helping admins trouble shoot their Active Directories and syncing with Office 365, but I have never setup an Active Directory server myself.

I setup the Domain Controller on a work server, and first went about assigning the roles to it.

![Windows Server Roles]({{ site.url }}/assets/roles.PNG)

Once that was handled it was pretty easy to setup and configure it as a forest. I set it up as subdomain.ponderth.at (actual subdomain left out for security).

Talking to a colleague this was not 100% a necessary step, but I think long term, this is similar to how many of our customers have theirs configured.

To add all of my domains to the domains and trusts section of Active Directory.

![Windows Server Roles]({{ site.url }}/assets/domainsandtrusts.png)

This allows you to set the UPN Sufix as necessary for the objects you are creating.

Surprisingly the least intensive portion of the whole setup was to install Azure AD Sync and then get it to start syncing with my tenant. I did run into a duplication issue I had not seen before where instead of it syncing to my main mailbox, it created a new unlicensed user with a bunch of numbers in the username.

Removing the user in AD, running a delta sync and then re-syncing after demoting my user down from Global Admin, corrected this behavior.
