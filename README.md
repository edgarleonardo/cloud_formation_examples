# Cloudformation: Automation vs Manual Work

In this article I am going to explain the advantages of automating our infraestructure in AWS using Cloudformation. First I am going to start off with a little comparison among Manual Work and Automation and how the automations can makes us more productives in our daily basis.


# Automation vs Manual Work

The majority of the companies that start working in the Cloud started  using the management console or ***Manual Work*** to create their infrastructure in the cloud but sooner or later we started facing some issues with the manual configuration, this are:

**High costs:** managing the infrastructure manually is inefficient because of the less controls.

**Low Quality:** any wrong configuration affect the applications and the final customer because in the manual work is too easy make mistake.

**Low Flexibility:** Any change on the infrastructure is complex because there isn't standarized automations that could help. 

***Automations***, in the other hands, are the way to follow, they helps us converting the best practices in guides to follow and  avoid the failure repetion, giving us:

**Better productivity:** replacing the manual work improves the efficiency of the whole team.

**Testing:** We are able to test our infrastructure's changes and avoid production problems.

**Shared Knowledge:** The way to manage the infrastructure is in code and is more easy to manage and maintain besides, the team is able to knows from others member benefiting the company overall.
  

## Cloudformation

Managing infrastructure in an automated way is on important key to success in AWS, the automations helps us improve the quality, reduce costs and improve flexibility but you may be asking your self: 

How can I automate my infrastructure?

The answer is simple, Cloudformation. 

Cloudformation is a service tool  offered by AWS to describe the infrastructure in code, you don't need to know any programming language if you don't want because the configuration can be made using simple json files.

But, how is possible that a Json file transforms into infrastructure on AWS?

Well, this is because the AWS API which is the magic wound that creates all those componenets once we configure on que Json files. In order to be able to create your template in AWS once prepared, you are going to need to publish through the webpage or the AWS CLI (this one need to be installed on your machine and you need to create a token to be able to access to the resources).
