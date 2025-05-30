FROM jupyter/datascience-notebook


# RUN pip install xgboost lightgbm

# ポート公開
EXPOSE 8888

# CVXOPTライブラリをインストールする
RUN conda update -y -n base -c  conda-forge conda \
&&  conda install -y -c conda-forge cvxopt \
&& pip install --upgrade pip \
# とりあえずこれ↓はいけそう
&&  pip install gym 
# これはいけなさそう↓. python3.11 に非対応っぽい
# && conda install -c conda-forge -y gym \ 
# && conda install -y -c conda-forge pygame

#コンテナ起動後のユーザをrootにする
# ref:https://qiita.com/SolKul/items/32443fb4452f7194bb8c
USER root

RUN rm -rf ~/.cache/matplotlib\
&&  apt-get update \
&&  apt-get install -y fonts-noto-cjk \
    fonts-ipaexfont \
&&  fc-cache -fv
