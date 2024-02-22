---
title: "How to improve your whatsapp status quality"
datePublished: Thu Feb 22 2024 03:07:31 GMT+0000 (Coordinated Universal Time)
cuid: clswn7ir600020bk0a8s5gvfl
slug: improve-whatsapp-status-quality
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708571457974/73c1417e-e801-4367-9626-36940f2d8248.png
tags: software-architecture, computer-science, whatsapp, technical-writing-1, whatsapp-tips

---

Let's keep this simple and straight to the point. You want to know what I found, I also want to share this. But hey, I wouldn't only tell you just this though, I like to geek about the technicals, you would have to hear that as well. So, it's a 2-for-1 treat tonight. Let's get started and to Business.

### Why is this possible now?

One primary reason why this is now possible and wasn't before, is because Whatsapp introduced the HD media file transfer feature.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708510500922/5cff10b0-c6ec-4ad9-8c16-87c63e6a9241.png align="center")

Around mid to late last year, Whatsapp introduced the HD transfer feature allowing users send images, videos or any other files at a higher quality by enabling the HD option when sending.

The [Verge](https://www.theverge.com/2023/8/17/23835641/whatsapp-hd-photo-video-compression) and [Techcrunch](https://techcrunch.com/2023/08/17/whatsapp-adds-support-for-hd-photos-says-hd-video-coming-soon/) provides more information about that update, if you are interested in that.

HD stands for High Definition, this means the media(image or picture) is at a higher resolution as compared to SD(Standard Definition) or other lesser media resolution/quality. This makes it look better. It is not the best quality there is, but it is an improvement to what has always been offered by Whatsapp.

In a previous [article](https://ebode.hashnode.dev/whatsapp-quality-reduction), I explained why Whatsapp reduces the quality of files you transfer, and how it saves them millions of dollars annually in running costs. Reading that should help you understand that this new feature comes at a cost to Whatsapp and why they can't just give you the best quality for your file transfers.

This workaround involves using this HD feature provided by Whatsapp for sending files, to also upload files on your Whatsapp status, therefore improving quality by at around x2 to x5 depending on the file type.

### The workaround

**\- First Approach (Failed)**

I tried two different approach to achieve this, the first failed. It seemed like Whatsapp figured what I was trying to do, and ignored the fact that I had set the image to HD, it compressed the hell out of the file as usual and posted it to my status without any improvement in the quality.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708512078111/d1facb54-fb64-4b98-9c1a-61af2f9c34d6.png align="center")

The image above shows the approach to the first failed attempt to improve status quality.

**\- Second Approach (Passed)**

I know Whatsapp does some message and media management, and tries to be efficient with those, by not letting you upload the exact same file over and over to their server, therefore using up unnecessary storage space, which can quickly add up.

They do a type of file caching(I would get into that later), to avoid storing duplicate file on their server. This caching approach is what made this approach work.

Let's get into that. The steps to recreate this is shown below.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708520918450/7700d75f-e856-46ea-9112-38ed5eca700f.png align="center")

1. Click the "add a contact to text" (button), you can actually send a message to yourself which is the least intrusive option.
    
2. The first option in there is to "message yourself", which is what we would use. This was officially introduced last year also.
    
3. You click the "add media" button, which is how you select the HD version of the file you want to send, and send it to yourself.
    
4. I have selected an image and have clicked on the HD icon, to push up the transfer quality.
    
5. I send that image to myself in the DM, a lot happens behind the scene with just this action, but I would get to that later.
    
6. This shows the HD image tag on the image to show the quality is HD.
    
7. I click on the forward button for that particular media already in my personal message box.
    
8. On the forward option, I select to my status.
    
9. This shows a box where I can add a body of text or "caption" to the image.
    

The last slide shows the image uploaded to my status with a higher resolution(quality), as opposed to just sharing the image normally without pasing the HD option

Posting this way to your status can be done for any type of media allowed by Whatsapp to be pushed up to HD.

### **How do you know this works?**

Ahhh yes! This is a very valid question. That image above is assumed to be of better quality till it can be proven. This is what would be done here..

To prove that this approach to updating media on Whatsapp actually improves the quality, there are two tests involved, the visual test and the size test.

* **Visual Test**
    
    For the visual test, all I have to do is post the same images side by side, one using the HD the other following the regular approach. This is the major reason why you would actually do this, to see a visual improvement in the quality of your post. Unforunately, I would not be able to highlight the differences on here, this is due to the fact that, this platform performs its own image compression when uploaded and would tamper with the quality of the images being compared. But you can do this yourself and find the difference.
    
* **Size Test**
    
    This is where we can fully confirm the image quality difference. To get to this, you first need to know that the higher the quality of a media, the larger the size of that media. A picture that's just regular quality may be 1Megabyte(1 MB) in size, while that same image in clearer quality and higher resolution would **most likely** be larger in size, around 1.5 to 3Megabytes(1.5-3MB). This outlines the difference in resolution. Also take note of the fact I said most likely, not always. There are lots of compression algorithms out there that could reduce the size of a media file and leave the quality as good(lossless compression), these defy those logic.
    
    Let me show you the size differences in the images and videos I uploaded to my Whatsapp status with the two different approach.
    
    This section was powered by **Adunni's** device.
    

To get the sizes of the files, you need to know that every Whatsapp status you ever view has to be downloaded off Whatsapp's server and be saved on your phone for 24hrs or for as long as that status is kept up by the poster. To achieve this, I posted this to my status and to ensure that my local environment has no effect on the size, I reached out to another Whatsapp user and there we investigated the sizes of the files.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708559056050/5c66379f-b06e-47b1-91d0-6ef513d5fe25.png align="center")

1. Arrow 1 points to the size of the first image, when it is posted to my Whatsapp status without the HD approach I outlined earlier. This is how we mostly post status everyday, the regular way. The size of that image is **93.61 KiloBytes**, which has been compressed down by Whatsapp's compression algorithm in-app, that image has therefore lost a lot of its quality, which is obvious in its appearance.
    
2. Arrow 2 points to the size of the second image which I posted using the HD method. The size is **548 Kilobytes**, which is about 6times the size of the first image, that means the quality of the image is a lot better compared to the first.
    
3. Arrow 3 points to the size of a video I posted using the same HD approach, the size of the video is **4.87 MegaByte**. I did this to show it also works for vides as well and improves their quality as well.
    
4. Arrow 4 point to the size of that same video, but the video was posted the same way we all post videos on our Whatsapp status everyday. Its size is **1.93 Megabyte**, about 2 and a half lesser in size to the video in the first approach, showing how much lesser in quality it is in comparison with the first video.
    

I think at this point, I have been able to show you the difference, between posting normally, and using the HD approach and how much more better in quality it gets with this approach. One final thing I want to get to, is the How this works question. This would contain my assumed technicals of why and how this works.

### Why and How does this Work

Earlier in this article, I mentioned something something about caching. To explain caching, lets start on a familiar note. Have you ever noticed, that whenever you send a large file to a friend on whatsapp the first time, it takes quite a while to process, and send, but when you either forward or send that same file to someone else, it sends almost instantly. If you have never noticed this, quickly go try it out. Send around a 10MB file to friend A, then either forward or send that same file to friend B and see how fast/instantly the file sends the second time.

So, initially when I found out, I assumed what was happening, and guess I assumed correctly. But knowing that this would be a public article, and people would want to know what my statements are based on, I decided to dig around and find official information to back this assumption up. It's provided below.

**So what is happening?** The first time you send a message or file or just about anything on Whatsapp, most people think it goes straight to the device of whoever they are sending it to, nope, first it goes from your phone straight to whatsapp's server, where it stays and chills, before getting sent to the whoever's device you sent it to.

Why would they do this you hurriedly ask next. Okay, okay, I'll answer that to. Actually, there are some pretty good reasons for this, let me explain, the first being that, there are a lot of cases where the user you are sending the message to, isn't online due to either not been connected to the internet, or their device has a flat battery. If those messages are not first stored on Whatsapp servers and just sent directly to such user, the messages would never get delivered and just "fall off the internet".

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708567284055/cc45b075-ebc7-47b8-b0d6-6b4e949772b2.png align="center")

A snippet from Whatsapp on message/file storage. You can view it [here](https://www.whatsapp.com/legal/privacy-policy-eea#:~:text=We%20temporarily%20store%20your%20messages,we%20try%20to%20deliver%20it.)

Hopefully the image and the explanation I gave above, makes you understand one of the WHYs. On the privacy side, you might ask, doesn't this mean they can check my messages when it is on their servers? according to Meta(Whatsapp's parent company) our messages are encrypted end-to-end, and the keys are only on our device, which means if they tried to look at your message it'll look like garbage to them. I'm taking their word for that.

The second and most important reason why messages(texts/files) are also sent to their server, is to serve as a type of cache, now let's talk caching. Earlier, I asked if you noticed how files sent the first time take a longer time, while the same file sent the second and other times, takes lesser time.

The first time you send the file, it is not sent to the user directly as we earlier mentioned, it is first stored on Whatsapp's server, then a link to that file is sent to the user, that's why they have a download option, so when they click download, they can get access to that file and save it on their device.

Remember now that from the most recent image above, Whatsapp says they keep files/messages for a while. Now, even after the user has downloaded that file, that file still stays on their server for a period of time determined by their server. If you then decide to send that same file to another person, within the time the file is still on the serve, and whatsapp can verify that nothing changed and it's the same file(most likely through a hash check), rather than having you send that file up again to the server, they tell your phone, "Hey we have this file already, just tell the user it's sent(your phone ticks sent almost instantly)", then the same link sent to the first user you initially sent that file to, is also sent to this new person you're sending the file to, and they can download if they want to. This saves both you from wasting data to send the same file again to their server and Whatsapp from having to give up extra space to store duplicate files.

Also, the moment Whatsapp deletes the file from their server, you get that error message on Whatsapp when you try to download, where they tell you to "Ask whoever sent the file to resend it".

This, is one definition to caching. "Temporarily saving data copies somewhere, so it can be accessed and retrieved faster and more efficiently".

You might then think, but they have enough space on their servers right? But the moment you realize that they have around a billion daily active users and a large number of these persons including you and I, all send files every now and then in Kilobytes, Megabytes and Gigabytes, you'll know that they save Terabytes on Terabytes of server space per second with just this approach and it's very very reasonable to.

**So how does this and the HD Whatsapp Status thing relate?**

If you haven't made the connection yet, here it is. So the first time you send that HD media to yourself, it gets sent to Whatsapp's servers like every other message.

The next step you take, is to forward that message to your status right?

So Whatsapp asks the server, do we have that picture, the server responds, "yes yes, we do, it's even in HD". Whatsapp rather than letting you resend another copy of that media file, instead creates a download link to that same HD file on their server, and lets all of your contacts have access to the file, but this time on your status.

Voila, mission accomplished, connection created.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708569404224/1c008be1-6434-4198-a136-9fdf9f9c8bb1.gif align="center")

It's a long write-up, but if you got here, I am guessing it was a good read. If you actually found this to be a good and useful read, Please share with others who you think might find this useful and interesting as well.

> **Thank you.**