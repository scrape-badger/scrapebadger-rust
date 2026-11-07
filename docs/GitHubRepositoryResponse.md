# GitHubRepositoryResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**repository** | [**models::GitHubRepositoryIdentity**](GitHubRepositoryIdentity.md) |  | 
**latest_commit** | Option<[**models::GitHubLatestCommit**](GitHubLatestCommit.md)> |  | [optional]
**readme** | Option<[**models::GitHubRepositoryReadme**](GitHubRepositoryReadme.md)> |  | [optional]
**files** | Option<[**Vec<models::GitHubRepositoryFile>**](GitHubRepositoryFile.md)> |  | [optional]
**languages** | Option<[**Vec<models::GitHubRepositoryLanguage>**](GitHubRepositoryLanguage.md)> |  | [optional]
**latest_release** | Option<[**models::GitHubRepositoryRelease**](GitHubRepositoryRelease.md)> |  | [optional]
**contributors** | Option<[**Vec<models::GitHubRepositoryAccount>**](GitHubRepositoryAccount.md)> |  | [optional]
**contributors_truncated** | Option<**bool**> |  | [optional]
**dependents** | Option<[**Vec<models::GitHubRepositoryAccount>**](GitHubRepositoryAccount.md)> |  | [optional]
**dependents_truncated** | Option<**bool**> |  | [optional]
**funding** | Option<[**models::GitHubRepositoryFunding**](GitHubRepositoryFunding.md)> |  | [optional]
**community_files** | Option<[**Vec<models::GitHubCommunityFile>**](GitHubCommunityFile.md)> |  | [optional]
**metadata_available** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


