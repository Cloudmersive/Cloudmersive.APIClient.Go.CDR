# \FileSanitizationApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**File**](FileSanitizationApi.md#File) | **Post** /cdr/sanitization/file | Content Disarm and Reconstruction on a File
[**FileAdvanced**](FileSanitizationApi.md#FileAdvanced) | **Post** /cdr/sanitization/file/advanced | Advanced Content Disarm and Reconstruction on a File
[**FileToPdf**](FileSanitizationApi.md#FileToPdf) | **Post** /cdr/sanitization/file/to/pdf | Content Disarm and Reconstruction on a File with PDFA Output
[**FileToPdfAdvanced**](FileSanitizationApi.md#FileToPdfAdvanced) | **Post** /cdr/sanitization/file/to/pdf/advanced | Advanced Content Disarm and Reconstruction on a File with PDFA Output


# **File**
> string File(ctx, optional)
Content Disarm and Reconstruction on a File

Processes the input file via CDR to produce a secured output file.  Input content is parsed, disarmed, and then reconstructed into a new output file with the same file format as the input.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***FileSanitizationApiFileOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FileSanitizationApiFileOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **optional.Interface of *os.File**| Input document, or photos of a document, to extract data from | 

### Return type

**string**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FileAdvanced**
> string FileAdvanced(ctx, optional)
Advanced Content Disarm and Reconstruction on a File

Processes the input file via CDR to produce a secured output file with advanced scan options and response headers containing scan metadata.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***FileSanitizationApiFileAdvancedOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FileSanitizationApiFileAdvancedOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowExecutables** | **optional.Bool**| Set to false to block executable files (EXE, DLL, etc.) | 
 **allowInvalidFiles** | **optional.Bool**| Set to false to block files that are not valid for their detected type | 
 **allowScripts** | **optional.Bool**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | 
 **allowPasswordProtectedFiles** | **optional.Bool**| Set to false to block password-protected files | 
 **allowMacros** | **optional.Bool**| Set to false to block files containing macros. Office macro removal still runs regardless. | 
 **allowXmlExternalEntities** | **optional.Bool**| Set to false to block XML files with external entity references (XXE) | 
 **allowInsecureDeserialization** | **optional.Bool**| Set to false to block files with insecure deserialization patterns | 
 **allowHtml** | **optional.Bool**| Set to false to block HTML files | 
 **allowUnsafeArchives** | **optional.Bool**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | 
 **allowOleEmbeddedObject** | **optional.Bool**| Set to false to block files with embedded OLE objects | 
 **allowUnwantedAction** | **optional.Bool**| Set to false to block files with unwanted actions | 
 **restrictFileTypes** | **optional.String**| Comma-separated list of allowed file extensions (e.g., \&quot;.pdf,.docx,.xlsx\&quot;). Files not matching will be blocked. | 
 **inputFile** | **optional.Interface of *os.File**| Input document to CDR process | 

### Return type

**string**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FileToPdf**
> string FileToPdf(ctx, optional)
Content Disarm and Reconstruction on a File with PDFA Output

Processes the input file via CDR to produce a secured PDF/A output file.  Input content is parsed, disarmed, and then reconstructed into a new PDF/A output file.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***FileSanitizationApiFileToPdfOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FileSanitizationApiFileToPdfOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **optional.Interface of *os.File**| Input document, or photos of a document, to extract data from | 

### Return type

**string**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **FileToPdfAdvanced**
> string FileToPdfAdvanced(ctx, optional)
Advanced Content Disarm and Reconstruction on a File with PDFA Output

Processes the input file via CDR to produce a secured PDF/A output file with advanced scan options and response headers containing scan metadata.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***FileSanitizationApiFileToPdfAdvancedOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a FileSanitizationApiFileToPdfAdvancedOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowExecutables** | **optional.Bool**| Set to false to block executable files (EXE, DLL, etc.) | 
 **allowInvalidFiles** | **optional.Bool**| Set to false to block files that are not valid for their detected type | 
 **allowScripts** | **optional.Bool**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | 
 **allowPasswordProtectedFiles** | **optional.Bool**| Set to false to block password-protected files | 
 **allowMacros** | **optional.Bool**| Set to false to block files containing macros. Office macro removal still runs regardless. | 
 **allowXmlExternalEntities** | **optional.Bool**| Set to false to block XML files with external entity references (XXE) | 
 **allowInsecureDeserialization** | **optional.Bool**| Set to false to block files with insecure deserialization patterns | 
 **allowHtml** | **optional.Bool**| Set to false to block HTML files | 
 **allowUnsafeArchives** | **optional.Bool**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | 
 **allowOleEmbeddedObject** | **optional.Bool**| Set to false to block files with embedded OLE objects | 
 **allowUnwantedAction** | **optional.Bool**| Set to false to block files with unwanted actions | 
 **restrictFileTypes** | **optional.String**| Comma-separated list of allowed file extensions (e.g., \&quot;.pdf,.docx,.xlsx\&quot;). Files not matching will be blocked. | 
 **inputFile** | **optional.Interface of *os.File**| Input document to CDR process | 

### Return type

**string**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

