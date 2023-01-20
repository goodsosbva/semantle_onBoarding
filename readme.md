# 시맨틀 — 단어 유사도 추측 게임

이 레포지터리는 Johannes Gätjen의 [Semantlich](http://semantlich.johannesgaetjen.de/)
([소스코드](https://github.com/gaetjen/semantle-de))를 포크하여,
한국어로 플레이할 수 있도록 수정한 것입니다.
- - -
### Setup (환결 설정 작업 방법)

Download Word2Vec and dictionary data:

```bash
cd data
wget https://dl.fbaipublicfiles.com/fasttext/vectors-crawl/cc.ko.300.vec.gz
gzip -d cc.ko.300.vec.gz
wget https://github.com/spellcheck-ko/hunspell-dict-ko/releases/download/0.7.92/ko-aff-dic-0.7.92.zip
unzip ko-aff-dic-0.7.92.zip
```

Filter and save word2vec in DB

```bash
docker-compose run --rm --entrypoint python app filter_words.py
docker-compose run --rm --entrypoint python app process_vecs.py
```

(Optional) Regenerate secrets

```bash
docker-compose run --rm --entrypoint python app generate_secrets.py
```

Start server

```bash
docker-compose up
```

- - -
### 꼬맨틀 개선 프로젝트 소개

* 꼬맨틀 개선프로젝트 코드 해당 저장소에서 보실 수 있습니다. 😎
* semantle_onBoarding/frontend/ 확인하실 수 있습니다. 😋
* 구체적으로 프로젝트의 목적과 의의는 아래의 ppt에 정리 해놨습니다. 🤗
* [개발_꼬맨틀 리팩토링 프로젝트2.pptx](https://github.com/goodsosbva/semantle_onBoarding/files/10462773/_.2.pptx)

- - -
### 꼬맨트 데이터 시각화 + css 스타일링 작업 소개
* 작업에 관한 설명은 할 예정입니다!!😅 (코드 작업은 완료 됐음.)


