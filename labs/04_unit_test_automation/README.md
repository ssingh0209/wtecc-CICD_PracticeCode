# Integrate Unit Test Automation

This folder holds the files for the lab: _Integrate Unit Test Automation_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.

$ kubectl apply -f task.yaml

$ kubectl apply -f pipeline.yaml

$ tkn pipeline start cd-pipeline     -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git"     -p branch="main"     -w name=pipeline-workspace,claimName=pipelinerun-pvc     --showlog
PipelineRun started: cd-pipeline-run-p5dtc
Waiting for logs to be available...
[init : remove] Removing all files from /workspace/source ...

[clone : clone] + '[' false '=' true ]
[clone : clone] + '[' false '=' true ]
[clone : clone] + '[' false '=' true ]
[clone : clone] + CHECKOUT_DIR=/workspace/output/
[clone : clone] + '[' true '=' true ]
[clone : clone] + cleandir
[clone : clone] + '[' -d /workspace/output/ ]
[clone : clone] + rm -rf '/workspace/output//*'
[clone : clone] + rm -rf '/workspace/output//.[!.]*'
[clone : clone] + rm -rf '/workspace/output//..?*'
[clone : clone] + test -z 
[clone : clone] + test -z 
[clone : clone] + test -z 
[clone : clone] + /ko-app/git-init '-url=https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git' '-revision=main' '-refspec=' '-path=/workspace/output/' '-sslVerify=true' '-submodules=true' '-depth=1' '-sparseCheckoutDirectories='
[clone : clone] {"level":"info","ts":1673657702.0840273,"caller":"git/git.go:170","msg":"Successfully cloned https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git @ 581185ac7f89bcd9722793e1362f6f9f0240acf2 (grafted, HEAD, origin/main) in path /workspace/output/"}
[clone : clone] {"level":"info","ts":1673657702.150902,"caller":"git/git.go:208","msg":"Successfully initialized and updated submodules in path /workspace/output/"}
[clone : clone] + cd /workspace/output/
[clone : clone] + git rev-parse HEAD
[clone : clone] + RESULT_SHA=581185ac7f89bcd9722793e1362f6f9f0240acf2
[clone : clone] + EXIT_CODE=0
[clone : clone] + '[' 0 '!=' 0 ]
[clone : clone] + printf '%s' 581185ac7f89bcd9722793e1362f6f9f0240acf2
[clone : clone] + printf '%s' https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git

[lint : flake8] Collecting Werkzeug==2.1.2
[lint : flake8]   Downloading Werkzeug-2.1.2-py3-none-any.whl (224 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 224.9/224.9 KB 15.8 MB/s eta 0:00:00
[lint : flake8] Collecting Flask==2.1.2
[lint : flake8]   Downloading Flask-2.1.2-py3-none-any.whl (95 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 95.2/95.2 KB 50.3 MB/s eta 0:00:00
[lint : flake8] Collecting python-dotenv==0.20.0
[lint : flake8]   Downloading python_dotenv-0.20.0-py3-none-any.whl (17 kB)
[lint : flake8] Collecting gunicorn==20.1.0
[lint : flake8]   Downloading gunicorn-20.1.0-py3-none-any.whl (79 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 79.5/79.5 KB 53.3 MB/s eta 0:00:00
[lint : flake8] Collecting honcho==1.1.0
[lint : flake8]   Downloading honcho-1.1.0-py2.py3-none-any.whl (21 kB)
[lint : flake8] Collecting pylint==2.14.0
[lint : flake8]   Downloading pylint-2.14.0-py3-none-any.whl (485 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 485.0/485.0 KB 77.9 MB/s eta 0:00:00
[lint : flake8] Collecting flake8==4.0.1
[lint : flake8]   Downloading flake8-4.0.1-py2.py3-none-any.whl (64 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 64.1/64.1 KB 41.0 MB/s eta 0:00:00
[lint : flake8] Collecting black==22.3.0
[lint : flake8]   Downloading black-22.3.0-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (1.5 MB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.5/1.5 MB 25.3 MB/s eta 0:00:00
[lint : flake8] Collecting nose==1.3.7
[lint : flake8]   Downloading nose-1.3.7-py3-none-any.whl (154 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 154.7/154.7 KB 83.4 MB/s eta 0:00:00
[lint : flake8] Collecting pinocchio==0.4.3
[lint : flake8]   Downloading pinocchio-0.4.3-py3-none-any.whl (12 kB)
[lint : flake8] Collecting coverage==6.3.2
[lint : flake8]   Downloading coverage-6.3.2-cp39-cp39-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (210 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 210.7/210.7 KB 76.3 MB/s eta 0:00:00
[lint : flake8] Collecting codecov==2.1.12
[lint : flake8]   Downloading codecov-2.1.12-py2.py3-none-any.whl (16 kB)
[lint : flake8] Collecting httpie==3.2.1
[lint : flake8]   Downloading httpie-3.2.1-py3-none-any.whl (124 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 125.0/125.0 KB 72.3 MB/s eta 0:00:00
[lint : flake8] Collecting Jinja2>=3.0
[lint : flake8]   Downloading Jinja2-3.1.2-py3-none-any.whl (133 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 133.1/133.1 KB 75.2 MB/s eta 0:00:00
[lint : flake8] Collecting itsdangerous>=2.0
[lint : flake8]   Downloading itsdangerous-2.1.2-py3-none-any.whl (15 kB)
[lint : flake8] Collecting click>=8.0
[lint : flake8]   Downloading click-8.1.3-py3-none-any.whl (96 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 96.6/96.6 KB 59.4 MB/s eta 0:00:00
[lint : flake8] Collecting importlib-metadata>=3.6.0
[lint : flake8]   Downloading importlib_metadata-6.0.0-py3-none-any.whl (21 kB)
[lint : flake8] Requirement already satisfied: setuptools>=3.0 in /usr/local/lib/python3.9/site-packages (from gunicorn==20.1.0->-r requirements.txt (line 9)) (58.1.0)
[lint : flake8] Collecting tomlkit>=0.10.1
[lint : flake8]   Downloading tomlkit-0.11.6-py3-none-any.whl (35 kB)
[lint : flake8] Collecting mccabe<0.8,>=0.6
[lint : flake8]   Downloading mccabe-0.7.0-py2.py3-none-any.whl (7.3 kB)
[lint : flake8] Collecting tomli>=1.1.0
[lint : flake8]   Downloading tomli-2.0.1-py3-none-any.whl (12 kB)
[lint : flake8] Collecting platformdirs>=2.2.0
[lint : flake8]   Downloading platformdirs-2.6.2-py3-none-any.whl (14 kB)
[lint : flake8] Collecting astroid<=2.12.0-dev0,>=2.11.5
[lint : flake8]   Downloading astroid-2.11.7-py3-none-any.whl (251 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 251.2/251.2 KB 84.8 MB/s eta 0:00:00
[lint : flake8] Collecting typing-extensions>=3.10.0
[lint : flake8]   Downloading typing_extensions-4.4.0-py3-none-any.whl (26 kB)
[lint : flake8] Collecting dill>=0.2
[lint : flake8]   Downloading dill-0.3.6-py3-none-any.whl (110 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 110.5/110.5 KB 48.4 MB/s eta 0:00:00
[lint : flake8] Collecting isort<6,>=4.2.5
[lint : flake8]   Downloading isort-5.11.4-py3-none-any.whl (104 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 104.1/104.1 KB 60.5 MB/s eta 0:00:00
[lint : flake8] Collecting mccabe<0.8,>=0.6
[lint : flake8]   Downloading mccabe-0.6.1-py2.py3-none-any.whl (8.6 kB)
[lint : flake8] Collecting pyflakes<2.5.0,>=2.4.0
[lint : flake8]   Downloading pyflakes-2.4.0-py2.py3-none-any.whl (69 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 69.7/69.7 KB 48.0 MB/s eta 0:00:00
[lint : flake8] Collecting pycodestyle<2.9.0,>=2.8.0
[lint : flake8]   Downloading pycodestyle-2.8.0-py2.py3-none-any.whl (42 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 42.1/42.1 KB 30.2 MB/s eta 0:00:00
[lint : flake8] Collecting pathspec>=0.9.0
[lint : flake8]   Downloading pathspec-0.10.3-py3-none-any.whl (29 kB)
[lint : flake8] Collecting mypy-extensions>=0.4.3
[lint : flake8]   Downloading mypy_extensions-0.4.3-py2.py3-none-any.whl (4.5 kB)
[lint : flake8] Collecting colorama
[lint : flake8]   Downloading colorama-0.4.6-py2.py3-none-any.whl (25 kB)
[lint : flake8] Collecting requests>=2.7.9
[lint : flake8]   Downloading requests-2.28.2-py3-none-any.whl (62 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 62.8/62.8 KB 31.6 MB/s eta 0:00:00
[lint : flake8] Collecting requests-toolbelt>=0.9.1
[lint : flake8]   Downloading requests_toolbelt-0.10.1-py2.py3-none-any.whl (54 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 54.5/54.5 KB 38.1 MB/s eta 0:00:00
[lint : flake8] Requirement already satisfied: pip in /usr/local/lib/python3.9/site-packages (from httpie==3.2.1->-r requirements.txt (line 24)) (22.0.4)
[lint : flake8] Collecting Pygments>=2.5.2
[lint : flake8]   Downloading Pygments-2.14.0-py3-none-any.whl (1.1 MB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1.1/1.1 MB 110.4 MB/s eta 0:00:00
[lint : flake8] Collecting charset-normalizer>=2.0.0
[lint : flake8]   Downloading charset_normalizer-3.0.1-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (198 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 198.8/198.8 KB 81.4 MB/s eta 0:00:00
[lint : flake8] Collecting defusedxml>=0.6.0
[lint : flake8]   Downloading defusedxml-0.7.1-py2.py3-none-any.whl (25 kB)
[lint : flake8] Collecting multidict>=4.7.0
[lint : flake8]   Downloading multidict-6.0.4-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (114 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 114.2/114.2 KB 55.3 MB/s eta 0:00:00
[lint : flake8] Collecting rich>=9.10.0
[lint : flake8]   Downloading rich-13.0.1-py3-none-any.whl (238 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 238.1/238.1 KB 86.2 MB/s eta 0:00:00
[lint : flake8] Collecting wrapt<2,>=1.11
[lint : flake8]   Downloading wrapt-1.14.1-cp39-cp39-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (77 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 77.8/77.8 KB 48.1 MB/s eta 0:00:00
[lint : flake8] Collecting lazy-object-proxy>=1.4.0
[lint : flake8]   Downloading lazy_object_proxy-1.9.0-cp39-cp39-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (62 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 62.1/62.1 KB 41.3 MB/s eta 0:00:00
[lint : flake8] Collecting zipp>=0.5
[lint : flake8]   Downloading zipp-3.11.0-py3-none-any.whl (6.6 kB)
[lint : flake8] Collecting MarkupSafe>=2.0
[lint : flake8]   Downloading MarkupSafe-2.1.1-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (25 kB)
[lint : flake8] Collecting urllib3<1.27,>=1.21.1
[lint : flake8]   Downloading urllib3-1.26.14-py2.py3-none-any.whl (140 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 140.6/140.6 KB 75.4 MB/s eta 0:00:00
[lint : flake8] Collecting idna<4,>=2.5
[lint : flake8]   Downloading idna-3.4-py3-none-any.whl (61 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 61.5/61.5 KB 20.6 MB/s eta 0:00:00
[lint : flake8] Collecting certifi>=2017.4.17
[lint : flake8]   Downloading certifi-2022.12.7-py3-none-any.whl (155 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 155.3/155.3 KB 77.3 MB/s eta 0:00:00
[lint : flake8] Collecting PySocks!=1.5.7,>=1.5.6
[lint : flake8]   Downloading PySocks-1.7.1-py3-none-any.whl (16 kB)
[lint : flake8] Collecting commonmark<0.10.0,>=0.9.0
[lint : flake8]   Downloading commonmark-0.9.1-py2.py3-none-any.whl (51 kB)
[lint : flake8]      ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 51.1/51.1 KB 33.0 MB/s eta 0:00:00
[lint : flake8] Installing collected packages: nose, mypy-extensions, mccabe, honcho, commonmark, charset-normalizer, zipp, wrapt, Werkzeug, urllib3, typing-extensions, tomlkit, tomli, python-dotenv, PySocks, Pygments, pyflakes, pycodestyle, platformdirs, pathspec, multidict, MarkupSafe, lazy-object-proxy, itsdangerous, isort, idna, gunicorn, dill, defusedxml, coverage, colorama, click, certifi, rich, requests, pinocchio, Jinja2, importlib-metadata, flake8, black, astroid, requests-toolbelt, pylint, Flask, codecov, httpie
[lint : flake8] Successfully installed Flask-2.1.2 Jinja2-3.1.2 MarkupSafe-2.1.1 PySocks-1.7.1 Pygments-2.14.0 Werkzeug-2.1.2 astroid-2.11.7 black-22.3.0 certifi-2022.12.7 charset-normalizer-3.0.1 click-8.1.3 codecov-2.1.12 colorama-0.4.6 commonmark-0.9.1 coverage-6.3.2 defusedxml-0.7.1 dill-0.3.6 flake8-4.0.1 gunicorn-20.1.0 honcho-1.1.0 httpie-3.2.1 idna-3.4 importlib-metadata-6.0.0 isort-5.11.4 itsdangerous-2.1.2 lazy-object-proxy-1.9.0 mccabe-0.6.1 multidict-6.0.4 mypy-extensions-0.4.3 nose-1.3.7 pathspec-0.10.3 pinocchio-0.4.3 platformdirs-2.6.2 pycodestyle-2.8.0 pyflakes-2.4.0 pylint-2.14.0 python-dotenv-0.20.0 requests-2.28.2 requests-toolbelt-0.10.1 rich-13.0.1 tomli-2.0.1 tomlkit-0.11.6 typing-extensions-4.4.0 urllib3-1.26.14 wrapt-1.14.1 zipp-3.11.0
[lint : flake8] WARNING: Running pip as the 'root' user can result in broken permissions and conflicting behaviour with the system package manager. It is recommended to use a virtual environment instead: https://pip.pypa.io/warnings/venv
[lint : flake8] WARNING: You are using pip version 22.0.4; however, version 22.3.1 is available.
[lint : flake8] You should consider upgrading via the '/usr/local/bin/python -m pip install --upgrade pip' command.
[lint : flake8] {--count}:0:1: E902 FileNotFoundError: [Errno 2] No such file or directory: '{--count}'
[lint : flake8] {--max-complexity=10}:0:1: E902 FileNotFoundError: [Errno 2] No such file or directory: '{--max-complexity=10}'
[lint : flake8] {--max-line-length=127}:0:1: E902 FileNotFoundError: [Errno 2] No such file or directory: '{--max-line-length=127}'
[lint : flake8] {--statistics}:0:1: E902 FileNotFoundError: [Errno 2] No such file or directory: '{--statistics}'
[lint : flake8] ./service/__init__.py:9:80: E501 line too long (94 > 79 characters)
[lint : flake8] ./service/__init__.py:10:80: E501 line too long (80 > 79 characters)
[lint : flake8] ./service/routes.py:43:80: E501 line too long (83 > 79 characters)
[lint : flake8] ./service/routes.py:57:80: E501 line too long (80 > 79 characters)
[lint : flake8] ./service/routes.py:78:80: E501 line too long (81 > 79 characters)
[lint : flake8] ./service/routes.py:93:80: E501 line too long (81 > 79 characters)
[lint : flake8] ./service/common/error_handlers.py:35:80: E501 line too long (84 > 79 characters)
[lint : flake8] ./service/common/error_handlers.py:47:80: E501 line too long (86 > 79 characters)
[lint : flake8] ./service/common/log_handlers.py:34:80: E501 line too long (88 > 79 characters)

failed to get logs for task lint : container step-flake8 has failed  : [{"key":"StartedAt","value":"2023-01-14T00:55:09.257Z","type":3}]
