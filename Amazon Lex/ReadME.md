# Set Up Multiple Slots in a Lex Chatbot

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-ai-lex5)

**Author:** Nchindo Boris  
**Email:** nchindoboris37@gmail.com

---

## Build a Chatbot with Multiple Slots

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-lex5_67890123)

---

## Introducing Today's Project!

### What is Amazon Lex?

Amazon Lex is a service for building chatbots and voice assistants using natural language understanding and speech recognition. 
It's useful because it simplifies bot development, handles scaling, integrates with AWS, and allows seamless interactions with users in real-time.

### How I used Amazon Lex in this project

In this project, I used Amazon Lex to build or create an intent that lets me transfer money between accounts and learn about AWS CloudFormation

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how intuitive the visual builder in Amazon Lex was. It made designing and testing the conversation flow much simpler, allowing me to create and adjust the bot's logic without writing complex code.

### This project took me...

The project took me about a 2 hours to complete. Setting up the intents, integrating Lambda, and testing the bot took the most time, but the visual builder and pre-configured tools in Amazon Lex helped speed up the process significantly.

---

## TransferFunds

An intent I created for my chatbot was TransferFunds, which helps users transfer funds between bank accounts.
The bot prompts for details like the amount and destination account, then processes the request and confirms the successful transfer.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-lex5_67890123)

---

## Using multiple slots

For this intent, I had to use the same slot type twice. This is because I needed to collect the same kind of information more than once, like two different account numbers or amounts, to process the user's request properly.

I also learned how to create confirmation prompts, which are messages that ask users to confirm their input before proceeding. 
They help ensure accuracy by allowing users to review and verify details, reducing errors in actions like transactions or settings changes.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-lex5_97dc2351)

---

## Exploring Lex features

Lex also has a conversation flow feature that lets you control how the interaction progresses. It helps guide through different steps, making sure the conversation stays on track by managing intents and slots based on what the user says.

You could also set up your intent using a visual builder! A visual builder lets you design and organize your chatbot's conversation flow with a drag-and-drop interface, making it easier to create and manage intents, slots, and responses.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-lex5_12345678)

---

## AWS CloudFormation

AWS CloudFormation is a service that lets you set up and manage AWS resources using code. 
It simplifies creating and configuring things like EC2 instances or S3 buckets, making it easier to automate and replicate infrastructure across different environments.


I used CloudFormation to automate the setup of AWS resources needed for creating the bot, Amazon Lex and Lambda configurations. 
This made it easier to deploy and manage the bot's infrastructure consistently without doing everything manually.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-lex5_c4fc89af)

---

## The final result!

Re-building my bot with CloudFormation took me 10 minutes which is very much quicker than setting up manually

There was an error after I deployed my bot! The error was beacuse CheckBalance intent wasnʼt working. 
I fixed this by reviewing the Lambda function's configuration and ensuring the correct permissions and references were set.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-lex5_505be5b8)

---

## Using the visual builder

Using the visual builder, I added Get slot value card, Condition card, Go to intent card.
What this means for an end user is the possibility to check account balance or not

The new Get slot value card will trigger when transfer is completed.
This card will try to capture success or failure of the transfer
It also checks whether the user wants to check account balance.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-lex5_9cac15cd4)

---

---

