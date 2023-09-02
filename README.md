# Bitly Url Shortener

This action creates a short URL from Bit.ly for a given URL.

## Inputs

### `bitly_token`

**Required** Bit.ly API Token. 

### `long_url`

**Required** Full URL to be shortened.

### `bitly_custom_domain`

Optional custom domain that is configured with Bit.ly

### `link_title`

Optional title of the link to record in Bit.ly

## Outputs

### `bitly_link`

Shortened URL from Bit.ly

## Example usage

```yaml
jobs:
  shorten:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Bitly shortener
        id: shortener
        uses: intersecato/bitly-shortener@v1.0.0
        with:
          bitly_token: ${{ secrets.BITLY_TOKEN }}
          long_url: link
```
