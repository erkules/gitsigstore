# Des Debianpaket war buggy. Vielleicht das Binary selbst bauen
~~~
go install github.com/sigstore/gitsign@latest
git config --local commit.gpgsign true  # Sign all commits
git config --local tag.gpgsign true  # Sign all tags
git config --local gpg.x509.program gitsign  # Use gitsign for signing
git config --local gpg.format x509  # gitsign expects x509 args
~~~

Und nun zur Verifikation

~~~
 git verify-commit HEAD
~~~
