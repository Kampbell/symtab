# symtab

A generic symbol table for lexically/statically scoped languages. The library is slightly dependent on ANTLR parse tree types, ParserRuleContext, but you could strip these out if you want to use it without ANTLR and don't want the dependency.

Uses Java 8 (a little).

Grab the [latest jar](http://www.antlr.org/download/symtab-1.0.1.jar).

## Building / installing

It's just a bunch of Java code so you can compile it like any other pile of code in a development environment. **It requires Java 8**. 

The easiest method is to use maven:

```bash
$ cd symtab
$ javac -version
javac 1.8.0_31
$ mvn package
...
[INFO] Building jar: /Users/parrt/antlr/code/symtab/target/symtab-1.0.3-SNAPSHOT.jar
...
```

Or you can `mvn install` to have it placed into your `~/.m2` maven cache.

## Example

[Simple example from my prog lang course](https://github.com/parrt/cs652/tree/master/lectures/code/symtab)

## Releasing version

```bash
$ mvn deploy
$ mvn release:prepare
```

It will start out by asking you the version number and other stuff then update `pom.xml`.

Handy command to wack snapshots:

```bash
$ curl -v -u user:password -X DELETE https://oss.sonatype.org/content/repositories/snapshots/org/antlr/symtab
```
