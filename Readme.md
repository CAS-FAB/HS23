

## Sample solutions

I've implemented [quarto profiles](https://quarto.org/docs/projects/profiles.html) to facility rendering a verion with and a version without (default) sample solutions. To render, publish or preview a version with sample solutions append `--profile musterloesung` to the respective command, which is defined in `_quarto-musterloesung.yml`. This means, that there is no need for playing around with `echo` and `output` in the code chunks.


### Publishing 

Instead of overwriting the version without sample solution with the version with sample solutions, I've decided to publish the version with sample solutions to a different destination, namely `quarto-pub`. This way, I can test and view the sample solutions easily and can just keep the URL hidden until the course is over. See below to publish to the two destinations.


```
quarto publish gh-pages --no-prompt
<!-- quarto publish quarto-pub --profile musterloesung --no-prompt -->
```

### Authoring

To display certain text or code content only in the sample solutions, add it in the following manner. 

```
::::{.content-visible when-profile="musterloesung"}
:::{.callout-note}

```{r}
#| filename: Musterlösung
1+1
```

:::
::::

```