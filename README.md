needlstk: A system for expressing network performance queries

The name is a portmanteau of needle and stack to reflect the
goal of finding needles in a haystack. It is pronounced "needle stack"

QuickStart:

1. . setup.sh (Don't execute setup.sh, source it)
2. antlr4 -visitor perf_query.g4
3. javac *.java
4. Generate parse tree using
grun perf_query prog  example_queries/flowlet_hist.sql -gui
(should open up a window showing the parse tree)
5. Run compiler using
cat example_queries/flowlet_hist.sql | java -ea PerfQueryCompiler 2> /tmp/tree.dot
6. Generate expression tree using
dot -Tpng /tmp/tree.dot > /tmp/tree.png
