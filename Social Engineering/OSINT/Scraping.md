### Using with cURL to find part of a page by ID
`curl --silent https://example.com/ | htmlq '#get-help'`

### Find all the links in a page
`curl --silent https://example.com/ | htmlq href a`

### Get the text content of a post
`curl --silent https://example.com | htmlq --text .main`

### Remove a node before output
`curl --silent https://nixos.org/ | htmlq '.whynix' --remove-nodes svg <ul class="whynix">`

### Syntax highlighting with [`bat`](https://github.com/sharkdp/bat)
`curl --silent example.com | htmlq 'body' | bat --language html`