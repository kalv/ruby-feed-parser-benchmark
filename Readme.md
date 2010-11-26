# Ruby Benchmark of feed parsers

This a benchmark for different Ruby Libraries

Libraries tested:

* rfeedparser: [http://rfeedparser.rubyforge.org/](http://rfeedparser.rubyforge.org/)
* Syndication: [http://syndication.rubyforge.org/doc/](http://syndication.rubyforge.org/doc/)
* SimpleRSS: [http://simple-rss.rubyforge.org/](http://simple-rss.rubyforge.org/)
* MagicRSS: [http://github.com/astro/harvester/tree/master/mrss.rb](http://github.com/astro/harvester/tree/master/mrss.rb)
* Feedzirra: [https://github.com/pauldix/feedzirra](https://github.com/pauldix/feedzirra)

## Results from last commit
Ran on a MBP 2.53gz 4gb SSD

    ruby feed-parser-bench.rb 1000

    feedzirra => Average: 0.0278322427572428 (0 errors) RSS: 0.0260872052845528 Atom: 0.0295189980353635
    mrss => Average: 0.042981384305835 (7 errors) RSS: 0.039129512244898 Atom: 0.0467262599206349
    syndication => Average: 0.0495069849548646 (4 errors) RSS: 0.0398204020408163 Atom: 0.0588687712031558
    rfeedparser => Average: 0.452556951048951 (0 errors) RSS: 0.389084115853658 Atom: 0.513909868369352
    simplerss => Average: 1.29865328871129 (0 errors) RSS: 0.20822887195122 Atom: 2.35265881532417
    

## Original results

Feel free to run the benchmark on your computer to see/compare the results

Here is what I get for 1000 feeds (among the /feeds directory with my MBP 11/2008) and libxml (rfeedparser can make use of libxml or expat):

rfeedparser => Average: 0.491536916083916 (0 errors) RSS: 0.423777936991869 Atom: 0.557032825147347
syndication => Average: 0.0748718385155466 (4 errors) RSS: 0.058977287755102 Atom: 0.0902334358974358
simplerss => Average: 0.348966465534465 (0 errors) RSS: 0.158927489837398 Atom: 0.53265836345776
mrss => Average: 0.0573559627766599 (7 errors) RSS: 0.0519932346938776 Atom: 0.0625697261904762

With Expat :
mrss => Average: 0.0446699295774648 (7 errors) RSS: 0.0407380755102041 Atom: 0.0484925654761905
rfeedparser => Average: 0.396704025974026 (0 errors) RSS: 0.342670530487805 Atom: 0.448932866404715
syndication => Average: 0.0560052517552658 (4 errors) RSS: 0.0450482204081632 Atom: 0.0665948875739645
simplerss => Average: 0.279452683316683 (0 errors) RSS: 0.13230812195122 Atom: 0.421682789783891
