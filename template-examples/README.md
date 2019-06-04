This subdirectory contains a few examples of how to use the Coq-community [template](https://github.com/coq-community/templates).

The files here can be generated in the following way, assuming `t` is set to the template directory:

``` shell
for dir in aac-tactics chapar lemma-overloading; do
  for f in $t/default.nix.mustache $t/README.md.mustache $t/.travis.yml.mustache; do
    mustache $dir/meta.yml $f > $dir/${f%.mustache} && echo "$dir/${f%.mustache}"
  do
  mustache $dir/meta.yml $t/coq.opam.mustache > $dir/coq-$dir.opam && echo "$dir/coq-$dir.opam"
done
```
