# Purge Azure CDN

GitHub Action for purging an Azure CDN endpoint

## Example Usage

```yml
- name: Azure service principal login
  uses: azure/login@v1
  with:
    creds: ${{ secrets.AZURE_CREDENTIALS }}
- name: Purge Azure CDN
  uses: svanboxel/azure-purge-cdn@main
  with:
    cdn_endpoint: your-endpoint (without `.azureedge.net`)
    cdn_profile_name: your-cdn-profile-name
    resource_group: your-resource-group
- name: Azure service principal logout
  run: |
    az logout
```
