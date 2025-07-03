
# MPDI

## Creating a New Article

To create a new article using this format:

```bash
quarto use template rpruim/mdpi
```

This will create a new directory with an example document that uses this format.

## Using with an Existing Document

To add this format to an existing document:

```bash
quarto add rpruim/mdpi
```

Then, add the format to your document options:

```yaml
format:
  mdpi-pdf: default
```    

## YAML Options

### Authors

Quarto provides a rich set of YAML metadata keys to describe authors and their affiliations.
If you provide this information, the mdpi quarto template will do its best to use that 
information in perparing your document.
Unfortunately, the mdpi LaTeX package has a fairly brittle way of dealing with author 
information. If you want to fully comply with their design, you will probably need 
to provide the information as a LaTeX file specified by `author-block` in the YAML.
If this exists, it will be used in place of any code generated from the `author` section
of the YAML.

See the template and its accompanying `author-info.tex` for examples.


## Example

Here is the source code for a sample document: [template.qmd](template.qmd).

