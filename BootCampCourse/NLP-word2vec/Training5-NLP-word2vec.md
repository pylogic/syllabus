# Training 5: NLP tools - basics

Ganben

## overview

what is NLP: natural language processing. it is a classic computer science research field. it has plenty of technology, toolkit package and theories.

learning sources:

- lexical analysis on program language: [shlex](https://docs.python.org/3/library/shlex.html) [ply](http://www.dabeaz.com/ply/)
- [Regular expression](https://docs.python.org/3/library/re.html) lib of python
- [natural language toolkit](http://www.nltk.org/)

## regular expression
you can use regular expression tool to imply complex rules on texts.

- strip excessive space, symbols, or remove the specified content
- get important information, for example get a number from strings
- judge if the number is a telephone number or ID card number
- define the permitted text formats, e.g. a email address or a password complexity check

the re can imply on unicode string, bytecode etc. please pay attention to the difference between python2 and python3. they handle the text in different ways. the re module has different usage.

```
re.comple
re.search
re.match
re.split
re.findall
re.sub

```

## lexical analysis

`shlex` is a python internal lib to process shell like simple syntaxes. it is useful if you want run control files in `subprocess` module.

`ply` is a full functional lexical analysis and compiler tool. you can define a simple lex tool to identify a language grammar. the important concepts:

1. tokens
2. lexer
3. parsing rules
4. name space

you should understand the lexical analysis:

- the difference between a string and a command 'ls -l {}'.format(v)
- how to use shlex to safely process the variables in a command line operation
- what does the token mean in a shell command or python code?
- use `ply` to process strings that written in python grammar, include symbols at lease '=' and '+'

## NLTK.org
the project is a good introduction. you should know the following topics:

- how to process a sentence to a token list
- how to identify POS tag for each token
- how to identify the named entities in a sentence
- how to generate a syntax tree for a sentence

## Task

- use re lib to filter keywords from a text, replace them with * , the keyworks list is a dict
- build a lexer, that can analysis with python-like grammar(with very few keywords/tokens), generate a syntax tree
- use NLTK tool to distinguish two kind of article: romance article and a news article.