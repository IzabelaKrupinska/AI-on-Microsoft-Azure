{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "id": "KjYLTg",
    "name": "help",
    "description": ""
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnBeginDialog",
      "$designer": {
        "name": "BeginDialog",
        "description": "",
        "id": "v48zvV"
      },
      "actions": [
        {
          "$kind": "Microsoft.SendActivity",
          "$designer": {
            "id": "UsFjT0"
          },
          "activity": "${SendActivity_UsFjT0()}"
        }
      ]
    }
  ],
  "generator": "help.lg",
  "recognizer": "help.lu.qna",
  "id": "help"
}
