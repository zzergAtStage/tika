# BIARUM.COM

## Why?

This change is being made to address security concerns identified by Veracode AppScan.

## What?
We are removing classes that utilize vulnerable functionalities, specifically those involving open command-line calls. These calls pose a potential security risk and will be replaced with safer alternatives.

## Where?
By list:
### ExternalParser
ExternalParser.java in [org.apache.tika.parser.external2](tika-core/src/main/java/org/apache/tika/parser/external2)
removed step-by-step (from dependencies list):
[ExternalParserTest.java tika-core/src/test/java/org/apache/tika/parser/external2/ExternalParserTest.java ](tika-core/src/test/java/org/apache/tika/parser/external2/)
commited in test configurations:
* [TIKA-3557-exiftool-example.xml](tika-core/src/test/resources/org/apache/tika/config/)
* [TIKA-3557-no-output-parser.xml](tika-core/src/test/resources/org/apache/tika/config/)
* [TIKA-3557.xml](tika-core/src/test/resources/org/apache/tika/config/)

[ExternalParser.java](tika-core/src/main/java/org/apache/tika/parser/external2/)

### ExternalEmbedder
Removed [ExternalEmbedder.java](tika-core/src/main/java/org/apache/tika/embedder/)