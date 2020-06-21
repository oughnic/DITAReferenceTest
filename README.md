# DITAReferenceTest
Simple example demonstrating DITA Keys

## Structure
The driving map file is T1T2.ditamap.  This includes references to Topic 1 and Topic 2 but not Topic 3.  It also includes a resource-only map with references to online web pages for Topic 1, Topic 2 and Topic 3.

Topics 1 and 2 both reference Topic 3 (which isn't in the driving map).


|File |Notes|
|--|--|
|T1T2.ditamap|The driving map for publication|
|keys.ditamap|The resource-only map for providing external links for missing keys and defining keys for T1 and T2|
|Topic_1.dita|A topic file with references to T2 and T3|
|Topic_2.dita|A topic file with references to T1 and T3|
|Topic_3.dita|A topic file with references to T1 and T2|

## How it works
When resolving the key references, the publisher first checks the included content for keys.  For topic 1 and Topic 2, the keys are already in T1T2.ditamap.
When trying to resolve T3, the key is missing from the included topics but is defined in the keys.ditamap as a resource-only processing role.  This external resource is used for T3.
