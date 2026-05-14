# GitHub Action: Delete tag and release

Add following step to your workflow:

```yaml
- uses: dev-drprasad/delete-tag-and-release@v0.2.0
  with:
    tag_name: v0.1.0 #(required) tag name to delete 
    delete_release: true #(optional) default: true 
    repo: <owner>/<repoName> #(optional) target repository. default: repo running this action
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Privacy

This Action contacts Chainguard's licensing server to verify authorization. Connection metadata (IP address, GitHub repository identifier, timestamp, and any metadata encoded in the auth token) is transmitted to Chainguard, Inc. even if authorization is denied in accordance with our [Privacy Notice](https://www.chainguard.dev/legal/privacy-notice)
