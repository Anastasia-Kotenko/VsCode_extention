import * as vscode from 'vscode';

export function activate(context: vscode.ExtensionContext) {
    let disposable = vscode.commands.registerCommand('extension.countWords', () => {
        let editor = vscode.window.activeTextEditor;
        if (editor) {
            let text = editor.document.getText();
            let wordCount = countWords(text);
            vscode.window.showInformationMessage(`Word count: ${wordCount}`);
        }
    });

    context.subscriptions.push(disposable);
}

export function deactivate() {}

function countWords(text: string): number {
    let words = text.split(/\s+/);
    return words.length;
}
