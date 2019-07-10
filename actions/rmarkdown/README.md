## Render RMarkdown Projects

This GitHub action renders an [RMarkdown](https://rmarkdown.rstudio.com/) project. 


### Secrets

None.


### Environment Variables

- [**`R_LIBS`**](https://stat.ethz.ch/R-manual/R-devel/library/base/html/libPaths.html), a vector of paths prepended to existing `.libPaths()`.
    
    Defaults to `R_LIBS_WORKFLOW` (`[$HOME](https://developer.github.com/actions/creating-github-actions/accessing-the-runtime-environment/#filesystem)/lib/R/library`) where they persist over the run of the workflow.
    All earlier or later actions that have `R_LIBS_WORKFLOW` in their `.libPaths()` can install to or load from this path.
    
    For more details, read the vignette on action [isolation](/articles/isolation/).


### Arguments

None.


### Example Usage

```
action "Check Package" {
  uses = "r-lib/ghactions/actions/rmarkdown@master"
}
```