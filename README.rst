==============
乗りログあぷり
==============


目的
=====

Webブラウザーでコメントを投稿するWebアプリケーションの練習。


ツールのバージョン
====================

:Python:     3.6.2
:pip:        19.1.1


インストールと起動方法
========================

リポジトリーからコードを取得し、その下にvenv環境を用意します::

    $ git clone https://github.com/Prog1108/norilog
    $ cd norilog
    $ python3.6 -m --without-pip venv
    $ source venv/bin/activate
    (venv) $ curl -LO https://bootstrap.pypa.io/get-pip.py
    (venv) $ python get-pip.py
    (venv) $ rm get-pip.py
    (venv) $ deactivate
    $ source venv/bin/activate
    (venv) $ pip install .
    (venv) $ norilog
      * Running on http://127.0.0.1:8000/


開発手順
=========

開発用インストール
-------------------

1. チェックアウトする
2. 以下の手順でインストールする

     (venv) $ pip instal -e .

依存ライブラリ変更時
----------------------

1. ``setup.py``の``install_requires``を更新する
2. 以下の手順で環境を更新する::

    (venv) $ deactivate
    $ python3.6 -m venv --clear venv
    $ source venv/bin/activate
    (venv) $ pip install -e .
    (venv) $ pip freeze > requirements.txt

3. setup.pyとrequirements.txtをリポジトリーにコミットする
