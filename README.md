I made this while trying to find out how to use cohttp with Lwt, because the
documentation is very sparse. It's not an "actual" web application, but I hope
that by uploading it here, people who find themselves in the same situation of
having no idea how to start will at least be able to start out a little further
along than I did.

It compiles with `opam install lwt cohttp xmlm` as of August 12, 2015. I will
try to keep it up-to-date, but I can't make any guarantees. Hopefully by the
time it becomes out of date, there will be better documentation.

You also need to install [ppx_sexp](https://bitbucket.org/jyc/ppx_sexp) and
[sxmlm](https://bitbucket.org/jyc/sxmlm) to use the rendering methods I've
included, although those can easily be excised.

To build, use `ocamlbuild -use-ocamlfind main.native`.

# Tips

- [Merlin](https://github.com/the-lambda-church/merlin) is extremely helpful
  when documentation is lacking! Using `:TypeOf` (or `<mapleader>T` in Vim, or
  the equivalent in Emacs) to find the type of the thing under your cursor can
  save you a lot of time searching through MLIs. Of course, it's also
  useful in general.
- It is sometimes easier to pull a repository and then read MLIs than to try to
  use autogenerated HTML documentation, especially if the project has `.merlin`
  files. I used `ack` and `grep` to search for strings like `val create`.
- `ocamlbuild -documentation` is useful to find out to get a sketchy idea of
  what tags do what.
- The OCaml IRC channel on FreeNode, `#ocaml`, is very helpful!

// vim: tw=80 :
