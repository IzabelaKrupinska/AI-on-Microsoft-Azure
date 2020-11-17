{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "id": "XwtiZS",
    "name": "PeripherialHardwareFailure",
    "description": ""
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnBeginDialog",
      "$designer": {
        "name": "PeripherialHardwareFailure",
        "description": "",
        "id": "t85mqD"
      },
      "actions": [
        {
          "$kind": "Microsoft.TextInput",
          "$designer": {
            "id": "ujGJpe"
          },
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${TextInput_Prompt_ujGJpe()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.namemodel"
        },
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "mWNZDq"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_mWNZDq()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.snperipherial"
        },
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "t63ElX"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_t63ElX()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.snap"
        },
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "7eDVdZ"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_7eDVdZ()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.customersn"
        },
        {
          "$kind": "Microsoft.TextInput",
          "$designer": {
            "id": "rytzyd"
          },
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${TextInput_Prompt_rytzyd()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.adress"
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "s9sP5h"
          },
          "activity": "${SendActivity_s9sP5h()}"
        }
      ]
    }
  ],
  "generator": "PeripherialHardwareFailure.lg",
  "recognizer": "PeripherialHardwareFailure.lu.qna",
  "id": "PeripherialHardwareFailure"
}
