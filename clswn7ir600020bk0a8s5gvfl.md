---
title: "How to improve your whatsapp status quality"
datePublished: Thu Feb 22 2024 03:07:31 GMT+0000 (Coordinated Universal Time)
cuid: clswn7ir600020bk0a8s5gvfl
slug: improve-whatsapp-status-quality
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708571457974/73c1417e-e801-4367-9626-36940f2d8248.png
tags: software-architecture, computer-science, whatsapp, technical-writing-1, whatsapp-tips

---

Let's keep this simple and straight to the point. You want to know what I found, I also want to share this. But hey, I wouldn't only just tell you that though, I like to geek about the technicals, you would have to hear that as well. So, it's a 2-for-1 treat tonight. Let's get right into it.

### Why is this possible now?

One primary reason why this is now possible and wasn't before, is because Whatsapp introduced the HD media file-transfer feature.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708510500922/5cff10b0-c6ec-4ad9-8c16-87c63e6a9241.png align="center")

Around mid to late last year, Whatsapp introduced the HD transfer feature allowing users send images, videos or any other files at a higher quality by enabling the HD option when sending.

The [Verge](https://www.theverge.com/2023/8/17/23835641/whatsapp-hd-photo-video-compression) and [Techcrunch](https://techcrunch.com/2023/08/17/whatsapp-adds-support-for-hd-photos-says-hd-video-coming-soon/) provided more information about that update when it was released. You can check it out if you are interested in that.

HD stands for High Definition, this means the media(image or picture) is at a higher resolution as compared to SD(Standard Definition) or other lesser media resolution/quality. This makes it look better. It is not the best quality there is, but it is an improvement to what has always been offered by Whatsapp.

In a previous [article](https://ebode.hashnode.dev/whatsapp-quality-reduction), I explained why Whatsapp reduces the quality of files you transfer, and how it saves them into the millions, of dollars in running costs annually. Reading that should help you understand that this new feature comes at some cost to Whatsapp and why they can't just give the highest and best file transfer quality.

The higher quality status update workaround involves using this HD feature provided by Whatsapp for sending files.This improves quality by around x2 to x5 depending on the file type.

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

1. Click the "add a contact to text" (button), you can actually send a message to yourself which is the least disruptive option.
    
2. The first option in there is to "message yourself", which is what we would use. This was officially introduced last year also.
    
3. You click the "add media" button, which is how you select the HD version of the file you want to send, and send it to yourself.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708615754807/f12da442-bf9b-48f3-b59b-377ca56aab8b.png align="center")
    
4. I have selected an image and clicked the HD icon, to give it the best quality available.
    
5. I send this image to myself in the DM, a lot happens behind the scene with just this action, but we would get to that later.
    
6. This shows the HD image tag on the image to show the quality is HD.
    
7. I click on the forward button for that same picture I just sent internally.
    
8. On the forward option, I select to my status.
    
9. This provides a box where I can add a "caption" for that image.
    

The last slide shows that the image has been successfully uploaded to my status at the HD resolution quality, as opposed to just sharing the image without this option.

Posting this way to your status can be done for any media type allowed by Whatsapp.

### **How do you know this works?**

Ahhh yes! This is a very valid question. The image above is assumed to be of better quality, but how can this be proven?

To prove that this approach to updating media on Whatsapp actually improves the quality, there are two tests involved, the visual and size test.

* **Visual Test**
    
    For the visual test, all I have to do is post the same images side by side, with the first using the HD upload method, and the other,the regular status upload method we are all used to.
    
* Unforunately, I would not be able to highlight the differences on here, this is due to the fact that, this platform(hashnode) performs its image compression when uploaded here, this would tamper with the quality of the images being compared and make it very hard to make out any difference. But you can do this yourself and find the difference.
    

**Size Test**

This is where we can correctly confirm and prove there is difference in quality. Getting to this, you first need to know that the higher the quality of a media, the larger its size. For example, a regular quality picture may be around 1Megabyte(1 MB) in size, while that same image looking sharper and with higher resolution would "**most likely"** be larger in size, around 1.5 to 3Megabytes(1.5-3MB).

Take note of the fact I said most likely, not always, there are compression algorithms out there that could reduce the size of a media file and leave the quality as good as it orignally was, this is called a lossless compression, those defy this logic.

To show the size differences in the images and videos I uploaded images and videos to my Whatsapp status with the two different approach and pointed out the size differences.

> This section was powered by **Adunni's** device.

To get the sizes of the files, you need to know that every Whatsapp status you ever view has to be downloaded off Whatsapp's server and saved on your device for 24hrs or for as long as the poster keeps it up.

To achieve this, I posted this to my status and investigated the size of the files.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708559056050/5c66379f-b06e-47b1-91d0-6ef513d5fe25.png align="center")

1. **Arrow 1** points to the size of the first image posted to Whatsapp status without the HD approach. This is how we mostly post status everyday, the regular way. The size of the image is around **93.61 KiloBytes**, with its size and quality reduced by Whatsapp's in-app compression algorithm.
    
2. **Arrow 2** points to the size of the second image posted to status using the HD method. The size is around **548 Kilobytes**, which is about 6times the size of the first image, showing a meaningful improvement in the size and quality of the image with this approach.
    
3. **Arrow 3** points to the size of a video posted using the same HD approach, the size of the video is around **4.87 MegaByte**. This was done to show this method also works fine for vides as well and improves their quality.
    
4. **Arrow 4** point to the size of that same video, but this time posted without the HD approach. Its size on device is around **1.93 Megabyte**, about 2 and a half times lesser in size to the video in the HD approach. This shows how much lesser in size and quality it is in comparison to the first video.
    

I think at this point, I have been able to point out the difference in posting normally, and using the HD approach for your Whatsapp status post. This improves the quality of the media files being posted.

### Why and How does this Work?

Earlier in this article, I mentioned something something about caching. To explain caching, lets start on a familiar note.

Have you ever noticed, that whenever you send a large file to a friend on whatsapp the first time, it takes quite a while to process and eventually send. When you either forward or send that same file to someone else on your contact list, it sends almost instantly this time.

If you have never noticed this, go try this out. Send a file around 10MB in size to friend A, then either forward or send that same file to another friend B and see how fast/instantly the file is sent the second time.

So, initially when I found out, I just assumed what was happening and left it at that, but knowing that this would be a public article, and people would want to know what my statements are based on, I decided to dig around and find official information to back this assumption up.

**So what is happening?** The first time you send a message or file or just about anything on Whatsapp, most people think it goes straight to the device of whoever they are sending it to, nope, first it goes from your device straight to whatsapp's server, where it first stored before getting sent to the receiver's device it was sent to.

Why would they do this you ask next. Okay, okay, I'll answer that too. There are some pretty good reasons for this, the first being that, there are a lot of cases where the user you are sending a message or file to isn't online due to any number of reasons. If those messages are not first stored on Whatsapp servers and then sent to such user, the messages would never get delivered and just "fall off the internet", but after being saved on their server, it keeps trying to send the message from their server to the recipient device, till it succesfully does.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708567284055/cc45b075-ebc7-47b8-b0d6-6b4e949772b2.png align="center")

A snippet officially from Whatsapp on what I just explained. You can read it [here](https://www.whatsapp.com/legal/privacy-policy-eea#:~:text=We%20temporarily%20store%20your%20messages,we%20try%20to%20deliver%20it.)

The second other reason why messages(texts/files) are also sent to their server, is to serve as a type of cache, now let's talk caching.

I earlier mentioned that the first time you send a message, it is not sent to the user directly, it is first stored on Whatsapp's server. This same thing happens when you send a picture, video or any file type. This is first sent and stored on a Whatsapp server, then a link to that file is sent to the user(recipient), with a download option, when they click download, the file is downloaded from the server over to their device.

In the snippet above, Whatsapp says they keep files/messages for a while. That file you sent to another user still stays on their server for a period of time determined by their server. If you then decide to send that exact file to another person while the file is still held on the server, rather than having you send that file up again to their server, they tell your device, "Hey we still have that file(picture, video, audio, etc)”, and then your phone ticks “sent” almost instantly without having to re-upload the file.

The same link sent to the first user for that same file is then sent to this new person you're sending the file to, and they can download it, if they want to. This saves you from wasting data to send(re-upload) the same file again to their server and also saves Whatsapp from having to give up unnecessary space to store duplicate files.

The moment Whatsapp deletes a file from their server, you get an error message on Whatsapp when you try to download, telling you to "Ask whoever sent the file to resend it". You most likely have seen this.

This whole process is one definition to caching, "temporarily saving data copies somewhere, so it can be accessed and retrieved faster and more efficiently".

You might then think, but don't Meta have big and bad enough servers with enough space on their servers for all these? Yes, but also, the moment you realize that they have around a billion daily active users and a large percentage of these persons including you and I, send different files every now and then in Kilobytes, Megabytes and Gigabytes, you'll know that this save them Terabytes on Terabytes of server space per second with just this approach and it's very very reasonable to.

**So how does this and the HD Whatsapp Status thing relate?**

If you haven't made the connection yet, here it is. So the first time you send that HD media to yourself, it gets sent to Whatsapp's servers like every other message or file.

The next step you take, is to forward that message to your status right?

So Whatsapp asks the server, do we have that picture on our server? The server responds, "yes yes, we do, better still, it’s in HD quality". Whatsapp rather than letting you resend another copy of that same file, creates a download link to the same HD file on their server, and lets all of your contacts have access to the file, but this time on your status.

This, my friend, is how and why this HD status upload approach works.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708569404224/1c008be1-6434-4198-a136-9fdf9f9c8bb1.gif align="center")

It's a long write-up, but if you got here, I am guessing it was a good read. If you actually found this to be a good and useful read, Please share with others who you think might also find it useful and interesting as well.

> **Thank you.**