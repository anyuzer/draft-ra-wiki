# Automated Performance Testing

## Why

Automated Performance Testing based on [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/) has been added into the pipeline, so that application contributors/owners can keep an eye on how the application performs and block deployments that drop scores under their thresholds.

## What

Configure and run tests automatically in your pipeline (see [here](https://github.com/telusdigital/telus-isomorphic-starter-kit/tree/master/load-test) for more details).

## Next steps

- Our own WebPageTest server
- WebPageTest running in the pipeline with set thresholds for TTFB, load times, etc.

## References

- [Setting up a private instance of a WebPageTest server](https://github.com/marcelduran/webpagetest-api/wiki/Test-Specs)
- [WebPageTest - Continuous Integration](https://github.com/marcelduran/webpagetest-api/wiki/Test-Specs) 
