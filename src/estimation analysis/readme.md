
## - 폴더 안내
- windows : 윈도우용으로 제작, mac용이랑 다른점 경로 부분만 있음 나머지는 같음
- mac : 맥용으로 제작, windows용이랑 다른점 경로 부분만 있음 나머지는 같음

### 1. 설명

- 파일 설명

:  SNN을 이용한 모델을 구현한 파일 (main.py)

: 구글 클라우드 플랫폼 음성인식(스피치) api를 이용한 파일(google_speech.py)

: 파이썬 웹 패키지 flask를 이용한 파일(run.py)


그외 폴더 설명

- model : 텐서플로우를 썼을때, 학습된 내용이 담긴 meta파일을 사용하였으나, 현재 프로젝트에서는 학습데이터의 wav를 행렬화 시켜놓은
csv파일을 만들고, x,y 2개 값으로 나눠서 저장해 두었음

- static : css파일과 이미지 파일이 들어 있음. flask에서 사용하는 이미지 파일들

- templates : 플라스크에서 사용하는 웹페이지 html 파일이 들어 있음

- tmp : 예측할 데이터를 저장할 폴더, 우리가 궁금했던 분류가 필요한 wav파일 저장소


- 아나콘도 모듈
###### import io
###### import os
###### import sys
###### import glob
###### import time
###### import random
###### import numpy
###### import pandas

- 새로 설치해야할 모듈
###### import librosa
###### import pydub
###### import sklearn
###### import google.cloud.speech
###### import flask

- 파일 추가로 impot한 파일들
###### import google_speech
###### import main
