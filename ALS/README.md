# Set recommendation system 

## Executive Summary
---
> user들이 명시적으로 남기는 평가 정보가 없는 상황에서, 제공받은 `item` 대비 `선택`한 기록을 기반으로 `Score`를 구성하고 이를 바탕으로 Collaborative Filtering 알고리즘 방식의 추천 시스템 구현.

하기 Mile Stone에 따라 project를 진행
1. score 점수 데이터를 기반으로, `user`들의 segments를 분리.
2. 동일한 segments 내 user들의 평점들을 근거로, target user의 미경험 아이템에 대한 평가를 추정.

### pre-requirements
- os: mac & window
- python: 3.8.10
    <details>
    <summary> library</summary>
    <div markdown="1">

    astroid==2.13.3 <br>
    asttokens==2.2.1 <br>
    backcall==0.2.0 <br>
    black==22.12.0 <br>
    click==8.1.3 <br>
    colorama==0.4.6 <br>
    comm==0.1.2 <br>
    contourpy==1.0.7 <br>
    cycler==0.11.0 <br>
    debugpy==1.6.6 <br>
    decorator==5.1.1 <br>
    dill==0.3.6 <br>
    executing==1.2.0 <br>
    fonttools==4.38.0 <br>
    ipykernel==6.20.2 <br>
    ipython==8.9.0 <br>
    isort==5.11.4 <br>
    jedi==0.18.2 <br>
    joblib==1.2.0 <br>
    jupyter_client==8.0.1 <br>
    jupyter_core==5.1.5 <br>
    kiwisolver==1.4.4 <br>
    lazy-object-proxy==1.9.0 <br>
    matplotlib==3.6.3 <br>
    matplotlib-inline==0.1.6 <br>
    mccabe==0.7.0 <br>
    mypy-extensions==0.4.3 <br>
    nest-asyncio==1.5.6 <br>
    numpy==1.24.1 <br>
    packaging==23.0 <br>
    pandas==1.5.3 <br>
    parso==0.8.3 <br>
    pathspec==0.11.0 <br>
    pickleshare==0.7.5 <br>
    Pillow==9.4.0 <br>
    platformdirs==2.6.2 <br>
    prompt-toolkit==3.0.36 <br>
    psutil==5.9.4 <br>
    pure-eval==0.2.2 <br>
    Pygments==2.14.0 <br>
    pylint==2.15.10 <br>
    pyparsing==3.0.9 <br>
    python-dateutil==2.8.2 <br>
    python-dotenv==0.21.1 <br>
    pytz==2022.7.1 <br>
    pywin32==305 <br>
    pyzmq==25.0.0 <br>
    scikit-learn==1.2.1 <br>
    scipy==1.10.0 <br>
    seaborn==0.12.2 <br>
    six==1.16.0 <br>
    stack-data==0.6.2 <br>
    threadpoolctl==3.1.0 <br>
    tomli==2.0.1 <br>
    tomlkit==0.11.6 <br>
    tornado==6.2 <br>
    traitlets==5.8.1 <br>
    typing_extensions==4.4.0 <br>
    wcwidth==0.2.6 <br>
    wrapt==1.14.1 <br>

    </div>
    </details>

<br>

## split segments of users
---

### get_user_segments.ipynb


