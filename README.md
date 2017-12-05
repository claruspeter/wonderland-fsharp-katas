# wonderland-fsharp-katas

Work in progress: one day, this will be an F# port of [@gigasquid](https://twitter.com/gigasquid)'s
[*wonderland-clojure-katas*](https://github.com/gigasquid/wonderland-clojure-katas).

![Alice and the tiny door](/images/alicedoor.gif)

>“Curiouser and curiouser!”
>-- ― Lewis Carroll, Alice in Wonderland

## How to Do the Katas

First, clone or fork this repo. All the katas are located in the folder `/wonderland-fsharp-katas/`. Each kata is an independent, self-contained F# script, and a companion instructions file (for example, alphabet-cipher.fsx and alphabet-cipher.md). Read the instructions, open the script file in your favorite editor or IDE, select all the code (<kbd>control</kbd>+<kbd>A</kbd>) and execute it (<kbd>Alt</kbd>+<kbd>Enter</kbd>) - and fix the code until the tests pass.

Before running any of the katas, you will need to download some dependencies, using [Paket](https://fsprojects.github.io/Paket/). Once your have cloned or forked the project, `cd .paket`, and run first `paket.bootstrapper.exe`, then `paket.exe install` to install the dependencies.

If you don't have F# installed yet, follow the instructions from the **use** section of [**fsharp.org**](http://www.fsharp.org).


## License

Copyright (c) 2015 Mathias Brandewinder, [MIT License](LICENSE).

Original Clojure version: Copyright © 2014 Carin Meier, distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.

Test edit.

![Alt text](https://g.gravizo.com/source/svg/custom_mark10?https%3A%2F%2Fraw.githubusercontent.com%2Fclaruspeter%2Fwonderland-fsharp-katas%2Fmaster%2FREADME.md)
<details> 
<summary></summary>
custom_mark10
digraph G {
    edge[fontsize=12];
    App[label="Seequent App"] ;
    TenDuke[label="10Duke",shape=rect,style=filled];
    Dynamo[shape=record,label="|Dynamo stream"];
    IdpProcessor;
    ResolveQueue[shape=record,label="|Resolve Queue"];
    Resolver;
    EventQueue[shape=record,label="|Event Queue"];
    EventProcessor;
    Database[shape=Mrecord,label="|Database|"];
    Api;
    MonitorPortal[shape=box3d];
    OneMinute[shape=none];
    App->TenDuke[label="checkout licence"];
    TenDuke->Dynamo[label="event"];
    Dynamo->IdpProcessor[label=trigger];
    IdpProcessor->EventQueue[label="rename events"];
    IdpProcessor->ResolveQueue[label="consumption events"];
    OneMinute->Resolver[style=dotted,label=tick];
    ResolveQueue->Resolver[label="read"];
    Resolver->TenDuke[dir="both",label="query for\n org/group"];
    Resolver->EventQueue[label="resolved\nconsumption"];
    OneMinute->EventProcessor[style=dotted,label=tick];
    EventQueue->EventProcessor[label="read"];
    EventProcessor->Database[label=update];
    Database->Api[label="query"];
    Api->MonitorPortal[label=display];
    }
  }
custom_mark10
</details>
