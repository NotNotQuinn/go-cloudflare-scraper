Cloudflare Challenge Solver
===========================

A port of [cloudflare-scrape](https://github.com/Anorov/cloudflare-scrape).

**⚠ Warning ⚠** : This is a fork and an attempt to make it work, 
it seems it does not work anymore and is more than 4 years out of date.
The original one might still work (havent tried), and has 
the latest bulk of commits from 2 years ago.

All dates relative to 2021-08-07 Y/M/D

Usage
-----

```go
package main

import (
    "github.com/NotNotQuinn/go-cloudflare-scraper"
)


func main() {
	scraper, err := scraper.NewTransport(http.DefaultTransport)
	if err != nil {
		log.Fatal(err)
	}

	c := http.Client{Transport: scraper}

	res, err := c.Get(ts.URL)
	if err != nil {
		log.Fatal(err)
	}

	body, err = ioutil.ReadAll(res.Body)
	res.Body.Close()
	if err != nil {
		log.Fatal(err)
	}
}
```

