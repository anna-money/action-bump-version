# Bump Version

Gets the latest release version and increases it.

## Examples

### Example workflow to release a new version with auto-incrementing version number

```yaml
    - uses: anna-money/action-bump-version@master
      id: bump
      with:
        token: ${{ secrets.GITHUB_TOKEN }}
    - run: echo ${{ steps.bump.outputs.new_tag }}
    - run: echo ${{ steps.bump.outputs.old_tag }}

```
