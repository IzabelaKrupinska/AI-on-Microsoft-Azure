{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "id": "RaXStY",
    "name": "FailureoftheIntrument",
    "description": ""
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnBeginDialog",
      "$designer": {
        "name": "FailureoftheInstrument",
        "description": "",
        "id": "yXrW4X"
      },
      "actions": [
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "s9uKMT"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_s9uKMT()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.clientnumber"
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "Gv5MDu"
          },
          "activity": "${SendActivity_Gv5MDu()}"
        },
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "EVF2Fr"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_EVF2Fr()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.numberintrument"
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "CfBXSL"
          },
          "activity": "${SendActivity_CfBXSL()}"
        },
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "dnk7Dh"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_dnk7Dh()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.phone"
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "g3a66Y"
          },
          "activity": "${SendActivity_g3a66Y()}"
        },
        {
          "$kind": "Microsoft.TextInput",
          "$designer": {
            "id": "wQ5IAL"
          },
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${TextInput_Prompt_wQ5IAL()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": ""
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "h9rjHj"
          },
          "activity": "${SendActivity_h9rjHj()}"
        }
      ]
    }
  ],
  "generator": "FailureoftheIntrument.lg",
  "recognizer": "FailureoftheIntrument.lu.qna",
  "id": "FailureoftheIntrument"
}
