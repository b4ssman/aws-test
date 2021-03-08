---

title: "Today I Learned a Thing"

date: 2021-02-24T10:07:35Z

draft: true

---

# Today I Learned a Thing

### What have I learned?

This is my fist time using Hugo. I have to say it's incredibly simple and I have been able to knock this site together in literally less than 10 minutes.

### What am I going to do with it?

I'm going to use this as the basis for a test site which I will create in AWS in order to get Signavio's site up and running.

### What does that involve?
The site pages will be statically generated HTML (although they are using MadCap and not Hugo). These pages will be hosted in S3.

The S3 pages will be attached to CloudFront (will read the docs on how to do that as I can't remember!)

This all needs to be built into a CircleCI pipeline (never done this before but I'm guessing it's not too hard)
