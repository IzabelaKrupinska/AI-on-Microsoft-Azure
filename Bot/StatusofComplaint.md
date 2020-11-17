{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "id": "WCLYyz",
    "name": "StatusofComplaint",
    "description": ""
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnBeginDialog",
      "$designer": {
        "name": "StatusofComplaint",
        "description": "",
        "id": "SrSfF2"
      },
      "actions": [
        {
          "$kind": "Microsoft.NumberInput",
          "$designer": {
            "id": "wdNrpA"
          },
          "defaultLocale": "en-us",
          "disabled": false,
          "maxTurnCount": 0,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${NumberInput_Prompt_wdNrpA()}",
          "unrecognizedPrompt": "",
          "defaultValueResponse": "",
          "property": "user.number",
          "validations": [
            "int(this.value) != null"
          ]
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "SHsq61"
          },
          "activity": "${SendActivity_SHsq61()}"
        },
        {
          "$kind": "Microsoft.DateTimeInput",
          "$designer": {
            "id": "vaCBGK"
          },
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${DateTimeInput_Prompt_vaCBGK()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.datecomplaint"
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "Ge9oXl"
          },
          "activity": "${SendActivity_Ge9oXl()}"
        },
        {
          "$kind": "Microsoft.TextInput",
          "$designer": {
            "id": "waNXPt"
          },
          "disabled": false,
          "maxTurnCount": 3,
          "alwaysPrompt": false,
          "allowInterruptions": false,
          "prompt": "${TextInput_Prompt_waNXPt()}",
          "unrecognizedPrompt": "",
          "invalidPrompt": "",
          "defaultValueResponse": "",
          "property": "user.emailstatus"
        },
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "cNiTpj"
          },
          "activity": "${SendActivity_cNiTpj()}"
        }
      ]
    }
  ],
  "generator": "StatusofComplaint.lg",
  "recognizer": "StatusofComplaint.lu.qna",
  "id": "StatusofComplaint"
}
