# flatten-monorepo
[![npm version](https://badge.fury.io/js/flatten-monorepo.svg)](https://badge.fury.io/js/flatten-monorepo) [![Build Status](https://travis-ci.org/cheshirecode/flatten-monorepo.svg?branch=master)](https://travis-ci.org/cheshirecode/flatten-monorepo) [![Coverage Status](https://coveralls.io/repos/github/cheshirecode/flatten-monorepo/badge.svg?branch=master)](https://coveralls.io/github/cheshirecode/flatten-monorepo?branch=master) [![Node.js Package](https://github.com/cheshirecode/flatten-monorepo/actions/workflows/npm-publish.yml/badge.svg)](https://github.com/cheshirecode/flatten-monorepo/actions/workflows/npm-publish.yml)

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
