# 마젠타 관련 설명

    미디파일들을 수집하여 데이터 셋을 만들고 이것을 머신러닝(RNN)을 이용해 새로운 창작물을 만들어 내는것.

    https://github.com/tensorflow/magenta 에 올려진 내용을 기반으로 음악파일(Midi file)을 생성


## 각 항목별 설명
###  1. Data File 

: 데이터셋 모으는 방법(크롤링을 통해서 Midi파일 수집)

    crawling1.py : 크롤링 방법 1
    crawling2.py : 크롤링 방법 2
    
     ※ 크롤링시 파일 다운로드 경로와 추후 마젠타 가동시에 사용할 input경로를 동일하게 지정해 주어야 한다.
     Midi파일의 경우는  그냥 사용하면 되지만 mp3나 wav파일일 경우는 컨버터 작업을 통해서 midi로 전환해야한다.
    
    
###  2. Setup 

: 마젠타를 설치하는 방법

    프로젝트를 진행하면서 가장 힘들었던 부분.
    마젠타를 설치하는 환경자체가 국한적이고 마젠타의 일반버전과 GPU버전을 동시에 설치해야 한다는 주의점이 있다.
    
    -- 파일설명
    
    setup.txt : 마젠타 환경설정 및 설치에 대한 전반적인 설명.

###  3. Magenta_step File 
: 준비된 데이터셋(Midi file)과 셋팅된  마젠타를 가지고 음악파일(Midi file)을 생성하는 방법
    
    -- 경로 설정 
    
    $ INPUT_DIRECTORY=/home/itwill02/바탕화면/it/rnb       # 학습시킬 노래 넣어둔 파일 
    $ SEQUENCES_TFRECORD=/tmp/notesequences.tfrecord    # tfrecord파일 생성할 곳 

    -- 파일 설명 
    
    create.txt : tfrecord 파일 생성 코드 > 학습,테스트 나누는 코드 > 학습시키는 코드 > 새로운 멜로디 뽑는 코드

###  4. Result File 

: 결과물 들어보기
    
    -- midi 파일 재생시켜 보기 

    $ sudo apt install timidity # timidity라는 패키지 이용 
    $ timidity {PATH} # PATH는 생성한 Midi파일의 경로를 지정해 준다.
    
    
###  5. Result_midi File 
: 결과물 

    -- 파일설명 : 
    
    zip file: 4종류의 midi 파일  : 각각 classic, rap, RnB, pop 장르의 10곡씩 결과물을 내어 보았다.
    wav file : 창작의 결과물인 midi 파일들을 goldwave라는 프로그램을 이용하여 합쳐 보았다. (drum_rnn,attetion_rnn사용)

