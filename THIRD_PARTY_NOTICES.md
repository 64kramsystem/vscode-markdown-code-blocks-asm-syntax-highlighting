# Third-party notices

## Bundled Assembly grammar

`syntaxes/nasm.tmLanguage.json` comes from [LucianIrsigler.nasm 1.3.1](https://github.com/lucianIrsigler/nasm-x86-syntax-highlighting), distributed by the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=LucianIrsigler.nasm). Original package path: `extension/syntaxes/nasm.tmLanguage.json`. Original file SHA-256: `3b73f19daf63767caef5dccb436df853294bfa8d281f21fa5a0635780ee89828`.

Modifications: JSON formatting is normalized; line-start anchors also accept the position after Markdown list/quote prefixes (`\G`); the root scope is renamed from `source.asm` to `source.markdown-code-blocks.assembly` to avoid conflicting with other extensions. All token scopes are preserved. The grammar is shipped in source form under MIT; see [the upstream license](licenses/nasm-MIT.txt). Other extension files remain under the root MIT [LICENSE](LICENSE).

To update the grammar, copy that file from a reviewed upstream release, apply the same scope rename and line-start anchor adaptations, refresh its version and SHA-256 here, preserve its license, and run `npm test`.

## Test fixture

`test/fixtures/markdown.tmLanguage.json` is copied unchanged from [VS Code 1.141.0](https://github.com/microsoft/vscode/blob/1.141.0/extensions/markdown-basics/syntaxes/markdown.tmLanguage.json), under the MIT license in `test/fixtures/LICENSE.txt`. Test fixtures are excluded from the extension package.
