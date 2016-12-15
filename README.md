
# go-boilerpipe

Golang port of the [boilerpipe](https://github.com/kohlschutter/boilerpipe) Java library written by Christian Kohlschütter.

Library used for the removal of website boilerplate, currently only supporting news article extraction.

See the [boilerpipe](boilerpipe/main.go) command-line tool for an example on how to use the library.


    import (
        "fmt"

        "github.com/jlubawy/go-boilerpipe"
        "github.com/jlubawy/go-boilerpipe/extractor"
    )

    doc, err := boilerpipe.NewTextDocument(r io.Reader)
    if err != nil {
        return nil, err
    }

    extractor.Article().Process(doc)

    fmt.Print(doc.Content())
