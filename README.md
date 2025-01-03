# AWS-Services-Fundamentals
This repository is basically for the fundamentals of AWS Services that are mainly used in Data Engineering or Software Engineering. It includes basic details of AWS Athena (sql-adhoc query service), EMR (computation Services), Redshift (data warehouse service), S3 (storage service) and others.

It has the details of almost all the AWS services which has been noted from official AWS skill builder learning site. It is a 50-Days learning challenge of learning AWS. Check out this link here for more info - https://skillbuilder.aws/


## 𝗟𝗘𝗔𝗥𝗡𝗜𝗡𝗚 𝗗𝗔𝗬 - 𝟭 What is AWS?
Everyone must be aware of this as it's a cloud platform offering numerous services to help organizations scale, innovate, lower costs etc. Multiple organizations have opted for AWS as its cloud platform to innovate better and earlier and/or move the existing solutions. AWS has the 𝗯𝗶𝗴𝗴𝗲𝘀𝘁 𝗺𝗮𝗿𝗸𝗲𝘁 𝘀𝗵𝗮𝗿𝗲 in the cloud, 𝘄𝗶𝘁𝗵 𝟯𝟮% 𝗼𝗳 𝘁𝗵𝗲 𝗺𝗮𝗿𝗸𝗲𝘁, followed by Microsoft's Azure Cloud and Google Cloud Platform (GCP). And since, my day-to-day work revolves around AWS, thought of diving deeper to get the detailed understanding about its technical terms and its services. 

So, I'm gonna start my 𝟱𝟬𝗗𝗮𝘆𝘀𝗢𝗳𝗟𝗲𝗮𝗿𝗻𝗶𝗻𝗴𝗔𝗪𝗦 challenge and will share my knowledge with all of you. Today's Day-1 and here is the learning.

𝘍𝘪𝘳𝘴𝘵 𝘵𝘩𝘪𝘯𝘨𝘴 𝘧𝘪𝘳𝘴𝘵. 𝘞𝘩𝘺 𝘥𝘰 𝘸𝘦 𝘦𝘷𝘦𝘯 𝘯𝘦𝘦𝘥 𝘈𝘞𝘚? 𝘞𝘩𝘢𝘵'𝘴 𝘵𝘩𝘦 𝘮𝘢𝘪𝘯 𝘣𝘦𝘯𝘦𝘧𝘪𝘵 𝘰𝘧 𝘵𝘩𝘪𝘴? 
There're 6 major things that every organization who's using AWS has the benefit of -

𝟭. 𝗣𝗮𝘆-𝗮𝘀-𝘆𝗼𝘂-𝗴𝗼 : You have to pay only for resources which you're using which isn't the case if you've on-premise system.

𝟮. 𝗕𝗲𝗻𝗲𝗳𝗶𝘁 𝗳𝗿𝗼𝗺 𝗺𝗮𝘀𝘀𝗶𝘃𝗲 𝗲𝗰𝗼𝗻𝗼𝗺𝗶𝗲𝘀 𝗼𝗳 𝘀𝗰𝗮𝗹𝗲 : Usage from hundreds of thousands of customers is aggregated in the cloud. So, AWS can achieve higher economies of scale and in turn lower pay-as-you-go prices.

𝟯. 𝗦𝘁𝗼𝗽 𝗴𝘂𝗲𝘀𝘀𝗶𝗻𝗴 𝗰𝗮𝗽𝗮𝗰𝗶𝘁𝘆 : With an on-premise system, we had to make a capacity decision for any application deployment. And, we might end up sitting idle with resources or working with less resource capacity. But, with AWS we don't have to. We can have as much and as little capacity as we want. And scale up and down as we need within few minutes.

𝟰. 𝗜𝗻𝗰𝗿𝗲𝗮𝘀𝗲 𝘀𝗽𝗲𝗲𝗱 𝗮𝗻𝗱 𝗮𝗴𝗶𝗹𝗶𝘁𝘆 : We can get the IT resources within minutes instead of weeks which gives us the dramatic increase in agility and time to developers to experiment something and innovate.

𝟱. 𝗥𝗲𝗮𝗹𝗶𝘇𝗲 𝗰𝗼𝘀𝘁 𝘀𝗮𝘃𝗶𝗻𝗴𝘀 : By removing "𝙪𝙣𝙙𝙞𝙛𝙛𝙚𝙧𝙚𝙣𝙩𝙞𝙖𝙩𝙚𝙙 𝙝𝙚𝙖𝙫𝙮 𝙡𝙞𝙛𝙩𝙞𝙣𝙜" companies can focus on projects that differentiate their business rather than maintaining data centers. We can focus on our customers rather than racking, stacking, and powering physical infrastructure.

𝟲. 𝗚𝗼 𝗴𝗹𝗼𝗯𝗮𝗹 𝗶𝗻 𝗺𝗶𝗻𝘂𝘁𝗲𝘀 : Applications can be deployed in minutes in multiple regions which can provide us lower latency and better customer experience at minimal cost.

**For more details:** https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html


## 𝗟𝗘𝗔𝗥𝗡𝗜𝗡𝗚 𝗗𝗔𝗬-𝟮 𝗔𝗪𝗦 𝗚𝗹𝗼𝗯𝗮𝗹 𝗜𝗻𝗳𝗿𝗮𝘀𝘁𝗿𝘂𝗰𝘁𝘂𝗿𝗲

𝗜𝗻𝗳𝗿𝗮𝘀𝘁𝗿𝘂𝗰𝘁𝘂𝗿𝗲 𝗲𝘅𝗶𝘀𝘁𝘀 𝗮𝘀 𝘁𝗵𝗲 𝗳𝗼𝘂𝗻𝗱𝗮𝘁𝗶𝗼𝗻 𝗼𝗳 𝗲𝘃𝗲𝗿𝘆 𝗰𝗹𝗼𝘂𝗱 𝗮𝗽𝗽𝗹𝗶𝗰𝗮𝘁𝗶𝗼𝗻. Infrastructure is basically the data centers and network connectivity. These data centers are connected with each other through redundant high speed and low latency. The 𝗰𝗹𝘂𝘀𝘁𝗲𝗿 of data centers is called 𝗔𝘃𝗮𝗶𝗹𝗮𝗯𝗶𝗹𝗶𝘁𝘆𝗭𝗼𝗻𝗲 (AZs). And, cluster of AZs is called 𝗥𝗲𝗴𝗶𝗼𝗻. 

Now, how do we decide which region is best for our application and/or customers who're using it. There're 𝗳𝗼𝘂𝗿 𝗺𝗮𝗷𝗼𝗿 𝗮𝘀𝗽𝗲𝗰𝘁𝘀 that we should keep in mind - 

𝟭. 𝗗𝗮𝘁𝗮 𝗖𝗼𝗺𝗽𝗹𝗶𝗮𝗻𝗰𝗲 : If we have regulations that the customers data should be kept in a specified geographic territory then we should choose a region that satisfies our data compliance requirements. No other factor is more important than this. 

𝟮. 𝗟𝗮𝘁𝗲𝗻𝗰𝘆 : If an application is sensitive to latency, then we should choose a region which is close to our user base which will prevent long wait times for our customers.

𝟯. 𝗣𝗿𝗶𝗰𝗶𝗻𝗴 : Prices vary from region to region due to the local economy and the physical nature of operating data centers. Internet connectivity, imported equipment costs, customs, real estate and other factors impact pricing. So, if we have a lower budget and no compliance or latency issues then it is better to choose a region with low cost.

𝟰. 𝗦𝗲𝗿𝘃𝗶𝗰𝗲 𝗔𝘃𝗮𝗶𝗹𝗮𝗯𝗶𝗹𝗶𝘁𝘆 : Not all the services are available in all the regions. So, based on our requirements whatever services we need to use we should see which region is providing that.

**For more details:** https://aws.amazon.com/about-aws/global-infrastructure/regions_az/


## 𝗟𝗘𝗔𝗥𝗡𝗜𝗡𝗚 𝗗𝗔𝗬-𝟯 𝗘𝗱𝗴𝗲 𝗟𝗼𝗰𝗮𝘁𝗶𝗼𝗻𝘀

Yesterday, we learned Proximity to Customers was one of the reasons to choose a Region. 

But, what if we have customers all over the world and we don't have any Regulatory Compliance to follow, or it has to be cheaper in cost or any specific AWS service use case. 

All we need is to reach our customers on time. We obviously can't have our application in multiple regions. So, what should we do?

AWS provides another service called 𝗔𝗪𝗦 𝗖𝗹𝗼𝘂𝗱𝗙𝗿𝗼𝗻𝘁 that gives us the opportunity to use 𝗲𝗱𝗴𝗲 𝗹𝗼𝗰𝗮𝘁𝗶𝗼𝗻𝘀. 

Edge location is a site that AWS CloudFront uses to 𝘀𝘁𝗼𝗿𝗲 𝗰𝗮𝗰𝗵𝗲𝗱 𝗰𝗼𝗽𝗶𝗲𝘀 of our data/content nearer to our customers' location for fastest delivery. 

So, whenever our customer tries to send a request then it fetches the data from the edge location no matter in which region our application is being deployed and data is stored. And, so there will be less to no latency.


