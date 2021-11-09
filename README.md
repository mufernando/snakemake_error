## Misunderstanding of modules?

From reading the [docs](https://snakemake.readthedocs.io/en/v6.10.0/snakefiles/modularization.html#modules), 
I thought that `main.snake` and `main2.snake` should be equivalent.
But when you try to run `main.snake`, it errors out as if `rule_a` hadn't been imported from `rule_a.snake`.
If you put that in the Snakefile then it works (`main2.snake` works).

See it for yourelf by running:

```
snakemake -p --snakefile main.snake --cores 1
snakemake -p --snakefile main2.snake --cores 1
```
