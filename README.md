# flatten-monorepo
[![npm version](https://badge.fury.io/js/flatten-monorepo.svg)](https://badge.fury.io/js/flatten-monorepo)


- Call from root folder of a project
```
CURRENT_PWD=$(pwd)
cd $TMPDIR
curl -sSL https://github.com/cheshirecode/flatten-monorepo/archive/master.zip --silent  -H 'Accept-Encoding: gzip,deflate' | tar xJ
cd flatten-monorepo-master/test
find monorepo-sample -print | sed -e 's;/*/;|;g;s;|; |;g' monorepo-sample
npx flatten-monorepo -r monorepo-sample
cd $CURRENT_PWD
unset CURRENT_PWD
```