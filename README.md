![example](images/example.png)



 EmoPic is combined by two words, **emo**tion + **pic**ture. EmoPic is a service which make changes in facial expressions through Korean text sentiment analysis. The sentiment analysis of Korean text is done by KoBert. The StarGan model is used for making facial expressions changes in pictures.

 Getting two inputs, text from utterance and a portrait photo, the EmoPic service categorizes the emotion implied in the input text in 6 different categories, then photoshops the input picture changing the face expression to the analyzed sentiment.

 Text sentiment analysis model is trained my utterance text and face expression changing model is trained by selfies of Koreans with various categories.

KoBert : https://github.com/SKTBrain/KoBERT

StarGan : https://github.com/yunjey/stargan

Team Levelup : [Kyeongwon Cho](https://github.com/F1RERED), [Youkyung Kang](https://github.com/KYK0328), [Taeyoung Kim](https://github.com/xaeyoungkim), [Hyoeun Lee](https://github.com/hyony2)

--------------

## Demonstration videos

<Data dashboard & Login & Signup>

https://github.com/F1RERED/EmoPic/assets/135773973/61e93ffb-eebf-42d3-9059-8b8cae0773e1

<Direct inputs & slang [Surprised]>

https://github.com/F1RERED/EmoPic/assets/135773973/c775bf38-3f76-487d-9bf8-3b71bc36df8a

<Using image2text(Naver Cloud OCR) API & screenshotlayer API [Sad]>

https://github.com/F1RERED/EmoPic/assets/135773973/099ccba4-24fc-425c-a9f8-05e704d2452c

<Distribution server(gunicorn & nginx)  [Angry])>

https://github.com/F1RERED/EmoPic/assets/135773973/8d35bc2f-85db-4c64-b293-568a52f172af

--------------------------------

## Files to be replaced

```
EmoPic

 └ mysite

	 └ .cache

		 └ kobert_v1.zip

	└ mysite

		└ surprise.pt


	└ stargan

		└ models

			└ 300000-D.ckpt

			└ 300000-G.ckpt

```

* kobert_v1.zip

  should be the trained model of kobert

+ surprise.pt

  should be the trained model of sentiment analysis based on kobert

+ 300000-D.ckpt & 300000-G.ckpt 

  should be the trained model of stargan 

-------

## API keys

* edit your views.py

service_view_naver_OCR_api_url = # Place your API keys here
service_view_naver_OCR_secret_key = # Place your API keys here

get your API key from this link :

https://www.ncloud.com/product/aiService/ocr



screenshotlayer_capture_screenshot_api_key = # Place your API keys here

get your API key from this link :

https://screenshotlayer.com/



service_result_view_removebg_API_key = # Place your API keys here

get your API key from this link :

https://www.remove.bg/ko



-------------------------

## Requirements

 Simulation based on python 3.7

 Versions in [requirements.txt](requirements.txt) are not mandatory. It's only the version used for our project.

 Please refer to the KoBert's and the StarGan's dependecies.

---------------------------------

## etc.

![certificate](images/[D27]_상장(문제해결빅데이터활용프로젝트)_최우수상_3조.jpg)
