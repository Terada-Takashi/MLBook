FROM jupyter/datascience-notebook


# RUN pip install xgboost lightgbm

# ポート公開
EXPOSE 8888

#コンテナ起動後のユーザをrootにする
# ref:https://qiita.com/SolKul/items/32443fb4452f7194bb8c
USER root

RUN rm -rf ~/.cache/matplotlib\
&&  apt-get update \
&&  apt-get install -y fonts-noto-cjk \
    fonts-ipaexfont \
&&  fc-cache -fv
