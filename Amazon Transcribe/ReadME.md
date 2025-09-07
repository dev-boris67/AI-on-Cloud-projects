# Transcribe Audio Files with AI

![Image](https://github.com/dev-boris67/AWS-Basics/blob/main/Project%20images/24.png?raw=true)

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-ai-transcribe)

**Author:** Nchindo Boris  
**Email:** nchindoboris37@gmail.com

---

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_o2p3q4r1)

---

## Introducing Today's Project!

In this project, I will demonstrate how to transcribe videos and audios using AWS services.

### Tools and concepts

Services I used were; Amazon Transcribe and S3. 
Key concepts I learnt include;
- Store a video with Amazon S3.
- Transcribe your video with Amazon Transcribe.
- Write custom vocabularies to improve your transcription's accuracy.
- Use custom filters to automatically remove unwanted words.
- Experiment with real-time transcription.

### Project reflection

This project took me approximately 40 minutes to complete. The most challenging part was adjusting 
the custom vocabulary and vocabulary filter to handle tricky terms and remove unwanted filler words effectively. It was most rewarding to see how these customisations significantly improved the transcription quality and to experience live transcription working smoothly

I did this project today because I wanted to learn how AI- 
powered transcription works, especially using AWS tools like Amazon Transcribe

---

## S3 and Transcribe

To set up for this project, I'm using an S3 bucket to store the video file I want to transcribe, as Amazon Transcribe requires media files to be stored in S3 to access and process them. 
The file Iʼm transcribing is now securely uploaded to the cloud, making it accessible for the transcription service to begin its work.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_k1l4m7n0)

---

## Run A Transcription Job

The steps to run a transcription job include uploading a media file to an S3 bucket, opening the Amazon Transcribe console, creating a new transcription job, selecting the general model type, and starting the job without any additional settings. Overall, this process took me just a few minutes, with the transcription itself taking around 1–2 minutes to complete. It was a straightforward and efficient setup, making it easy to get started with transcribing audio using AWS.

Amazon Transcribe uses model types to optimise transcription accuracy based on the nature of the audio content. These models are trained for specific use cases to better handle unique vocabulary, speech patterns, and background noise. 
Use cases of model types include the general model for everyday speech, the medical model for healthcare-related content, and the call analytics model for customer service and call centre recordings. Selecting the right model type ensures that the transcription is as accurate and relevant as possible for the given context.

You can customise a transcription further with subtitling, which adds subtitles and speaker partitioning.
Subtitles help people who are deaf, hard of hearing, or speak different languages to understand a video or audio. 
Speaker partitioning helps to label different speakers in an audio recording i.e. who said what.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_g0h1i2j3)

---

## Baseline Transcript Review

To start using Amazon Transcribe, I first ran a baseline transcription job, which means I transcribed the audio without applying any custom settings or enhancements. This is because it's important to see how well the service performs on its own, using just the raw audio. The baseline transcription acts as a reference point, helping me measure how much improvements like custom vocabularies or filters actually enhance the final transcription later on.

While reviewing the baseline transcript, I noticed several inaccuracies. For example, “repositories” was misspelt as “repositoriesies”, and technical terms like “403 Forbidden” were mis-transcribed as “4 or 3 forbidden”. Speech fillers like “um” were included, which can be distracting in the final text. Additionally, “player A” should have been capitalised to “Player A” to reflect its proper use as a title in the context of the video. These happened because transcription tools can struggle with unclear pronunciation, background noise, specialised vocabulary, or words not commonly found in their training data.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_s3t6u9v2)

---

## Custom Vocabulary

I can resolve transcription inaccuracies using a custom vocabulary, which is a personalised list of words and phrases that I want Amazon Transcribe to recognise correctly. A custom vocabulary improves transcription accuracy by helping the service identify specialised terms, technical jargon, acronyms, or unique phrases that arenʼt part of the default language model, ensuring they are transcribed properly and consistently.

To create an item in a custom vocabulary, you need to define two values. They are the Phrase, which is the exact word or term you want Amazon Transcribe to recognise, and DisplayAs, which is how you want that phrase to appear in the transcription. This helps ensure that words are both correctly identified and consistently formatted in the final transcript

My custom vocabulary defines specific terms and corrections to improve transcription accuracy, including fixing the misspelt “repositoriesies” to “repositories”, capitalising “player” to “Player”, and correcting “four-or-three-forbidden” to properly represent “403 Forbidden” without spaces or numbers.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_e3f4g5h6)

---

## Vocabulary Filters

Another feature in Transcribe is vocabulary filtering, which automatically removes or masks unwanted words or phrases from transcripts, such as sensitive information. Itʼs different from custom vocabularies because instead of teaching Transcribe to recognise and correctly display specific terms, vocabulary filters block or clean up words I donʼt want to appear in the transcription, making it a more efficient way to manage unwanted content. 

My vocabulary filter removes unwated text, i.e. common filler words like “um,” “uh,” “like,” and other unnecessary speech fillers that clutter the transcription. To set up this filter, I first created a plain text file listing these unwanted words, separated by commas, and then uploaded it to Amazon Transcribe to apply the filter during transcription.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_u7v8w9x0)

---

## Enhanced Transcription

### I ran a new transcription with my custom vocabulary and filtering settings

The enhanced transcription is better than the baseline because it correctly displays key terms from my custom vocabulary, such as properly capitalising Player A and fixing the spelling of repositories. It also removes filler words like “um” using the vocabulary filter, making the transcript cleaner and easier to read. Additionally, speaker partitioning helps separate who is speaking, which improves clarity in conversations. Although “403 Forbidden” is still incorrect, this shows that further customisation or training may be needed for highly technical terms. Overall, the transcription is noticeably more accurate than the baseline version.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_k1l2m3n4)

---

## Real Time Transcription

For my project extension, I experimented with real-time transcription, which converts speech to text instantly i.e. as the speaker is still talking.
This very useful feature for apps that want to offer live captioning and voice commands!

Even during real-time transcription, I was able to apply custom vocabulary and vocabulary filtering, which helped improve the recognition of specific terms and remove unnecessary filler words. Overall, compared to a standard transcription job, real-time transcription was faster and surprisingly effective, though there were still occasional inaccuracies with complex terms like “403 Forbidden”. Despite that, it performed well in recognising phrases from my custom setup, making it a powerful option for use cases like live captioning, voice assistants, or interactive applications.

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-ai-transcribe_a5b6c7d8)

---

---
