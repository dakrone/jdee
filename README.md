# JDEE

The JDEE is an add-on software package that turns Emacs into a
comprehensive system for creating, editing, debugging, and documenting
Java applications.

## About the project

As of 2015-07-13, https://github.com/jdee-emacs/jdee/ is the primary source repository.

Additional information can be found at http://jdee.sourceforge.net/rootpage.html and at https://github.com/jdee-emacs/jdee/wiki

## Requirements

Emacs 24.3 is the oldest version that JDEE can be expected to run in.

Building JDEE requires [Apache Ant](https://ant.apache.org/bindownload.cgi)

JDEE can use Beanshell for some operations - available from
```http://www.beanshell.org/```. Copy bsh-2.0b4.jar to
```$JAVA_HOME/jre/lib/ext```, or put it in CLASSPATH.

## Install from distribution

FIXME: need ELPA package

For more information, see ```doc/install.html```

## Build from source options

1. Available Ant targets: ```ant -p```
2. (_Always_) Run unit tests: ```ant test```
3. Run JUnit tests: ```ant test-java```
4. Build project: ```ant bindist```

To use this built distribution without installation, in your .emacs add:
```emacs-lisp
  (add-to-list 'load-path "/path/to/jdee/dist/jdee-2.4.2/lisp")
  (load "jde-autoload")
```

If hacking on jde lisp, it is better to build in the git-controlled
source directory, by adding:

```
build.lisp.dir=${project.dir}/lisp
```

to ```~/.jdee-config.properties``` (```%USERDATA%/.jdee-config.properties``` on Windows)
