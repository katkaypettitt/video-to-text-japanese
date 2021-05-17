# Video to Text (Japanese 日本語)

> Transcribes Japanese video to text. Videos may be short or long in length. 

## General info

This code converts video to text and performs some very light cleaning (i.e. adding punctuation, removing filler words, etc.) to provide a little bit of polish to the final product. Currently [April 2021], there is no easy way to do this for Japanese videos which does not use the Cloud. Alternatively, one could obtain the language data and train a model from scratch, but this is often not feasible for small teams or teams with limited resources. As such, this code utilises the IBM Cloud and their Watson Speech to Text service. They offer 500 free minutes/month. 

To run the code, you will need to create an IBM Cloud account and input the api key and url which can be found on your Watson Speech to Text page. You will also need to change the `input_filename` in the second cell (variable `command`) to the name of the video you would like to convert. Please make sure this video is saved in the same area as your Notebook file. 

The video conversion does not take too long, although this will vary depending on the specs of your machine. Converting a 1hr30 video took me 45 minutes. 

If you come across any issues when running the second cell (i.e. no wav file is outputted), then you may have issues with your ffmpeg installation. I found that running `!pip install ffmpeg`, a bad practice in itself (I recommend importing packages via sys), was insufficient. Installing ffmpeg via [Brew](https://brew.sh/) did the trick. 

The following files are included in this repo:

* `video-to-text-longfiles.ipynb`: code for videos longer than ~15 minutes
* `video-to-text-shortfiles.ipynb`: code for short videos

## Technologies

Python 3.7.6, ffmpeg 1.4, ibm-watson 5.1.0, and ibm-cloud-sdk-core 3.9.0

## Inspiration

Although there are many options and even whole packages for transcribing videos in certain languages (e.g. English), there are limited resources and documentation for Asian languages, including Japanese. This code has been developed to automate menial tasks and hopefully help others do the same.

## Contact

Created by [@katrinaalaimo](https://www.katrinaalaimo.com/). If you have any questions, feel free to contact me in English or Japanese!



**日本語版がなくて大変失礼いたします。ご質問などがございましたら、遠慮なくご連絡ください。**
