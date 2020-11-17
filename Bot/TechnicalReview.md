{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "id": "drt3Pg",
    "name": "TechnicalReview",
    "description": ""
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnBeginDialog",
      "$designer": {
        "name": "TechnicalReview",
        "description": "",
        "id": "dpFpkT"
      },
      "actions": [
        {
          "$kind": "Microsoft.ConfirmInput",
          "$designer": {
            "id": "cqz46j"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${ConfirmInput_Prompt_cqz46j()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "choiceOptions": {
            "includeNumbers": true,
            "inlineOrMore": ", or ",
            "inlineOr": " or "
          },
          "property": "user.confirm"
        },
        {
          "$kind": "Microsoft.IfCondition",
          "$designer": {
            "id": "BfKGcc"
          },
          "condition": "user.confirm==true",
          "elseActions": [
            {
              "$kind": "Microsoft.SendActivity",
              "$designer": {
                "id": "3ETWny"
              },
              "activity": "${SendActivity_3ETWny()}"
            }
          ],
          "actions": [
            {
              "$kind": "Microsoft.NumberInput",
              "$designer": {
                "id": "7nc8mm"
              },
              "defaultLocale": "en-us",
              "disabled": false,
              "maxTurnCount": 3,
              "alwaysPrompt": false,
              "allowInterruptions": false,
              "prompt": "${NumberInput_Prompt_7nc8mm()}",
              "unrecognizedPrompt": "",
              "invalidPrompt": "",
              "defaultValueResponse": "",
              "property": "user.number"
            },
            {
              "$kind": "Microsoft.SendActivity",
              "$designer": {
                "id": "Z1md5j"
              },
              "activity": "${SendActivity_Z1md5j()}"
            },
            {
              "$kind": "Microsoft.NumberInput",
              "$designer": {
                "id": "OaoDaM"
              },
              "defaultLocale": "en-us",
              "disabled": false,
              "maxTurnCount": 3,
              "alwaysPrompt": false,
              "allowInterruptions": false,
              "prompt": "${NumberInput_Prompt_OaoDaM()}",
              "unrecognizedPrompt": "",
              "invalidPrompt": "",
              "defaultValueResponse": "",
              "property": "user.numberinstr"
            },
            {
              "$kind": "Microsoft.SendActivity",
              "$designer": {
                "id": "KQhAGV"
              },
              "activity": "${SendActivity_KQhAGV()}"
            },
            {
              "$kind": "Microsoft.DateTimeInput",
              "$designer": {
                "id": "gEh5qx"
              },
              "disabled": false,
              "maxTurnCount": 3,
              "alwaysPrompt": false,
              "allowInterruptions": false,
              "prompt": "${DateTimeInput_Prompt_gEh5qx()}",
              "unrecognizedPrompt": "",
              "invalidPrompt": "",
              "defaultValueResponse": "",
              "property": "user.datereview"
            },
            {
              "$kind": "Microsoft.SendActivity",
              "$designer": {
                "id": "0m63oM"
              },
              "activity": "${SendActivity_0m63oM()}"
            }
          ]
        }
      ]
    }
  ],
  "generator": "TechnicalReview.lg",
  "recognizer": "TechnicalReview.lu.qna",
  "id": "TechnicalReview"
}
