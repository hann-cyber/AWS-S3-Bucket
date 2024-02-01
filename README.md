# Making Your First AWS S3 Bucket
A guide illustrating how to make your first bucket using Amazon Web Services S3. Buckets can be used to store data that can be accessed later on cloud storage! The data can also be encrypted, and can be made public or kept privately. Some popular uses are for big data analytics or disaster recovery backups. Another example, which I'll be illustrating is deploying a public facing website.

1. To start, I'll head over to the S3 service and click create a bucket.

<p align="center">
 <img src="https://i.imgur.com/Sd9uPtM.png">
</p>

Here, the bucket is successfully created.

<p align="center">
 <img src="https://i.imgur.com/9FDZknS.png">
</p>

2. Next, I add the desired files. So far, this is pretty similar to any other cloud based storage such as Microsoft OneDrive of Google Drive.

<p align="center">
 <img src="https://i.imgur.com/vlwvOcH.png">
</p>

To view the image I can click the "Open" button in the top right corner. But there's an issue with the public URL provided.

<p align="center">
 <img src="https://i.imgur.com/S8H03aI.png">
</p>

Here, I used the object URL link that was provided, which doesn't work since I didn't modify the access permissions. 

<p align="center">
 <img src="https://i.imgur.com/rjfg2HJ.png">
</p>

In this scenario I used the "open" button, and now you can see my Beagle rescues! The reason why this works differently is due to AWS providing a private tokenized link that grants me access to the file. Note: I blocked my token info.

<p align="center">
 <img src="https://i.imgur.com/elxjvFG.png">
</p>

3. Make an allow public access policy:

To make the image accessible to the public I go to the permissions tab, where you can notice there's a "block all public access" setting. AWS keeps this on by default but, for my project I'll be editing this setting. This will come into play in future guides.

<p align="center">
 <img src="https://i.imgur.com/YamHxV7.png">
</p>

AWS policies use JSON fiels to grant or deny access; this is the same for IAM policies. Here, seasoned technicians can write up their own JSON file manually but, AWS also provides an easy to use policy generator.

My policy allows all clients to access the image. Note: Action: "GetObject", Effect: "Allow", and Principal: "*". The asterisk (*) implies anyone, and GetObject infers retrieving an object which, in this case, is an image file.

<p align="center">
 <img src="https://i.imgur.com/MKVDzp7.png">
</p>

Once the policy is saved, some warning tags show up to illustrate to cloud admins that the information is publicly accessible.

<p align="center">
 <img src="https://i.imgur.com/7iK22qH.png">
</p>

Now, the image can be seen using the public URL.

<p align="center">
 <img src="https://i.imgur.com/6TydCtA.png">
</p>

All this information is required before being able to make a publicly accessible webpage which I have a write up for in my next project on [making a static webpage](http://github.com/hann-cyber/AWS-S3-StaticWeb)
