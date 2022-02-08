# Aspose-Blazor-Bug
Exposes bugs with Aspose in Blazor Webassembly

## Bugs Descriptions
[Cryptography bug](https://docs.microsoft.com/en-us/dotnet/core/compatibility/cryptography/5.0/cryptography-apis-not-supported-on-blazor-webassembly)

To fix the cryptography bug, Aspose should reference a web-friendly library mentioned on the article above.

Additionally, when running the tests I have on in `src-blazor\BlazorComponents\Components\BlazorArticleComment.razor`, you will notice that there are random null-pointer exceptions that occur. It is unclear if this is due to the crytography bug above, or if it is independent. I have tried various different properties to remediate the issue but they will not work, as you will see listed in the file listed.

## Running
To get this to run, all you have to do is cd to `src-blazor\AngularAdapterBuild`, run `dotnet build`, cd to `src-blazor\BlazorComponents`, and then run a `dotnet publish`. This will create the Angular components necessary, as well as publish the `_framework` folder over to be called in wasm within Angular.

To get the angular component to try and generate pdf's, hit 'print to console' button on one of the Blazor-generated comments.