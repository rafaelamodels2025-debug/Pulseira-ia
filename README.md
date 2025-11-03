# Pulseira-ia
Protótipo de uma pulseira de ia multimodal (geminni,azure,Galaxy aí)para automação social e holograma de certificado
    // See http://go.microsoft.com/fwlink/?LinkId=827846
    // for the documentation about the extensions.json format
    "recommendations": [
        "dbaeumer.vscode-eslint",
        "amodio.tsl-problem-matcher",
        "streetsidesoftware.code-spell-checker"
    ]
}// Place your settings in this file to overwrite default and user settings.
{
    "files.exclude": {
        "out": false // set this to true to hide the "out" folder with the compiled JS files
    },
    "search.exclude": {
        "out": true // set this to false to include "out" folder in search results
    },
    // Turn off tsc task auto detection since we have the necessary tasks as npm scripts
    "typescript.tsc.autoDetect": "off",
    // Help the cSpell extension find our configuration files (it doesn't import .yaml by default)
    "cSpell.import": ["./.vscode/cspell.yaml"],
    // Block committing directly to main branch
    "git.branchProtection": ["main"],
    // Keep files nice
    "files.trimTrailingWhitespace": true,
    "files.insertFinalNewline": truehttp://go.microsoft.com/fwlink/?LinkId=827846extensions.jsonfrom google import genai

client = genai.Client()

response = client.models.generate_content(
    model="gemini-2.5-flash",
    contents="Explain how AI works in a few words"
)
print(response.text