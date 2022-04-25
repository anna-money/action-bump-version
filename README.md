# Bump Version

Gets the latest release version and increases it.

## Input Variables

- **token** (`string`, required) - The GitHub token.
- **with_month** (`true|false`, optional) - Add the month number as a second part of the tag (e.g. 2022.5.10) (
  default: `false`).
- **add_tag** (`true|false`, optional) - Add a tag to the commit (default: `true`).

## Examples

### Example workflow to release a new version with auto-incrementing version number

```yaml
    - uses: anna-money/action-bump-version@master
      id: bump
      with:
        token: ${{ secrets.GITHUB_TOKEN }}
        with_month: false
        add_tag: false
    - run: echo ${{ steps.bump.outputs.new_tag }}
    - run: echo ${{ steps.bump.outputs.old_tag }}

```
