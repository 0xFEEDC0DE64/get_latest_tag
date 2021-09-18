# get_latest_tag
GitHub action to get the hash and name of the latest tag

## Example workflow

```yaml
name: Getting the tag name

on: push

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Get tag name
      id: get-tag-name
      uses: 0xFEEDC0DE64/get_latest_tag@main

    - name: Print tag info
      run: |
        echo "name of the tag is ${{ steps.get-tag-name.outputs.tag_name }}"
        echo "hash of the tag is ${{ steps.get-tag-name.outputs.tag_hash }}"
```

