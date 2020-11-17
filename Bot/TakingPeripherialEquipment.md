{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "id": "yGhyJF",
    "name": "TakingPeripherialEquipment",
    "description": ""
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnBeginDialog",
      "$designer": {
        "name": "TakingPeripherialHardware",
        "description": "",
        "id": "tl7PGd"
      },
      "actions": [
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "05YgOq"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_05YgOq()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.snperi"
        },
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "pZKINo"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_pZKINo()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.customer"
        },
        {
          "$kind": "Microsoft.TextInput",
          "$designer": {
            "id": "tFRqOD"
          },
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${TextInput_Prompt_tFRqOD()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.adr"
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "pzVY89"
          },
          "activity": "${SendActivity_pzVY89()}"
        }
      ]
    }
  ],
  "generator": "TakingPeripherialEquipment.lg",
  "recognizer": "TakingPeripherialEquipment.lu.qna",
  "id": "TakingPeripherialEquipment"
}
