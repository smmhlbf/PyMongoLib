# Project construct information

## I.Create python virtual environment

~~~ bash cli
python3 -m venv venv
source venv/bin/activate
python3 -m pip install --upgrade pip -ihttp://pypi.douban.com/simple --trusted-host pypi.douban.com
~~~

## II.Upgrad pip version in virtual enviroment

~~~ bash cli
pip --default-timeout=100 install -U setuptools==51.1.2(version of you needed)(search version from pypi.org) -ihttp://pypi.douban.com/simple --trusted-host pypi.douban.com
~~~

### II-1.Tsinghua university mirror host https://pypi.tuna.tsinghua.edu.cn/simple/

### II-2.Trusted host of tsinghua university command parameter use

~~~ bash cli
--trusted-host pypi.tuna.tsinghua.edu.cn
~~~

### II-3.Aliyun mirror host https://mirrors.aliyun.com/pypi/simple/

### II-4.Trusted host of aliyun command parameter use

~~~ bash cli
--trusted-host mirrors.aliyun.com
~~~

## III.Setvscode user snippets for python file default head inpython.json

### III-1.Set python file deault header information

~~~ json source code
    "HEADER": {
        "prefix": "header",
        "body": [
        "'''",
        "@Compile  : /venv/bin python3",
        "@Charset  : utf-8",
        "@File     : $TM_FILENAME",
        "@Time     : $CURRENT_YEAR-$CURRENT_MONTH-$CURRENT_DATE $CURRENT_HOUR:$CURRENT_MINUTE:$CURRENT_SECOND",
        "@IDE      : Visual Studio Code(MacOS)",
        "@Author   : your name",
        "@Contact  : your email",
        "@Version  : ${1:1.0}",
        "@License  : ㏇Copyright $your company",
        "@Desc     : ${2:None}",
        "'''",
        "",
        "# import lib list:",
        "$0",
        "",
        "",
        "if __name__ == '__main__':",
        "    pass",
        ""
        ],
        "description": "Add default python file custom header information."
    }
~~~

### III-2.Set python file default def function with one parameter,same of more as your wish

~~~ json source code
    "1DEF": {
        "prefix": "1def",
        "body": [
            "def ${1:funcName}(${2:parameterName}: ${3:parameterType}) -> ${4:returnType}:",
            "    '''",
            "    ${5:functionDescription}",
            "    :param: ${2:parameterName}: ${6}",
            "    :return: ${7}",
            "    '''",
            "    pass$0",
            "",
            ""
        ],
        "description": "Add default def custom function with one parameter."
    }
~~~

### III-3.Set python file default custom class

~~~ json source code
    "CLASSNOIMPL": {
        "prefix": "niclass",
        "body": [
            "class ${1:className}:",
            "    '''",
            "    ${2:classDescription}",
            "    '''",
            "    pass$0",
            "",
            ""
        ],
        "description": "Add no implementing other any object custom class."
    }
~~~

### III-4.Set python file default class implementing one super class,same of more as your wish

~~~ json source code
    "CLASSONEIMPL": {
        "prefix": "oiclass",
        "body": [
            "class ${1:className}(${2:superClassName}):",
            "    '''",
            "    ${3:classDescription}",
            "    :implementing: ${2:superClass}",
            "    '''",
            "    pass$0",
            "",
            ""
        ],
        "description": "Add one implementing other any object custom class."
    }
~~~

### III-5.Set python file default class method with one parameter,same of more as your wish

~~~ json source code
    "1CDEF": {
        "prefix": "1cdef",
        "body": [
            "def ${1:funcName}(self, ${2:parameterName}: ${3:parameterType}) -> ${4:returnType}:",
            "    '''",
            "    ${5:functionDescription}",
            "    :param: ${2:parameterName}: ${6}",
            "    :return: ${7}",
            "    '''",
            "    pass$0",
            "",
            ""
        ],
        "description": "Add default def custom method with one parameter."
    }
~~~

## IV.Include pymongo package to control mongo database by python

~~~ json source code
pip install pymongo -ihttp://pypi.douban.com/simple --trusted-host pypi.douban.com
~~~