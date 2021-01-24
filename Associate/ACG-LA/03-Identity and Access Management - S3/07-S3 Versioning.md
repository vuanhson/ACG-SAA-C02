## S3 Versioning

### Using Versioning With S3
- Stores all versions of an object (including all writes and even if you delete an object)
- Great backup tool.
- Once enabled, Versioning cannot be disabled, only suspended.
- Integrates with Lifecycle rules
- Versioning’s MFA Delete capability, which uses multi-factor authentication, can be used to provide an additional layer of security.
- If you made an object public then upload new version, the new version is NOT PUBLIC, old version still public accessible
- To recover deleted object, go to object version list then delete the version named: "delete marker"