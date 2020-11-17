{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "id": "pwd71s",
    "name": "MakeComplaint",
    "description": ""
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnBeginDialog",
      "$designer": {
        "name": "MakeComplaint",
        "description": "",
        "id": "R0xvCQ"
      },
      "actions": [
        {
          "$kind": "Microsoft.ConfirmInput",
          "$designer": {
            "id": "fMaUC8"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${ConfirmInput_Prompt_fMaUC8()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "choiceOptions": {
            "includeNumbers": true,
            "inlineOrMore": ", or ",
            "inlineOr": " or ",
            "inlineSeparator": ", "
          },
          "property": "user.confirmed"
        },
        {
          "$kind": "Microsoft.IfCondition",
          "$designer": {
            "id": "kjPaJS"
          },
          "condition": "user.confirmed==true",
          "elseActions": [
            {
              "$kind": "Microsoft.TextInput",
              "$designer": {
                "id": "RyScZz"
              },
              "disabled": false,
              "maxTurnCount": 3,
              "alwaysPrompt": false,
              "allowInterruptions": false,
              "prompt": "${TextInput_Prompt_RyScZz()}",
              "unrecognizedPrompt": "",
              "defaultValueResponse": "",
              "validations": [],
              "property": "user.email"
            },
            {
              "$kind": "Microsoft.SendActivity",
              "$designer": {
                "id": "8fQ5Bu"
              },
              "activity": "${SendActivity_8fQ5Bu()}"
            }
          ],
          "actions": [
            {
              "$kind": "Microsoft.SendActivity",
              "$designer": {
                "id": "0lLGEn"
              },
              "activity": "${SendActivity_0lLGEn()}"
            }
          ]
        }
      ]
    }
  ],
  "generator": "MakeComplaint.lg",
  "recognizer": "MakeComplaint.lu.qna",
  "id": "MakeComplaint"
}
