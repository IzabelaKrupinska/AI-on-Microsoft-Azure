{
  "$kind": "Microsoft.AdaptiveDialog",
  "$designer": {
    "$designer": {
      "name": "RocMed",
      "description": "Bot for the medical company Roc Med.",
      "id": "UuTG7N"
    }
  },
  "autoEndDialog": true,
  "defaultResultProperty": "dialog.result",
  "triggers": [
    {
      "$kind": "Microsoft.OnConversationUpdateActivity",
      "$designer": {
        "id": "376720",
        "name": "WelcometoRocMed"
      },
      "actions": [
        {
          "$kind": "Microsoft.Foreach",
          "$designer": {
            "id": "518944",
            "name": "Loop: for each item"
          },
          "itemsProperty": "turn.Activity.membersAdded",
          "actions": [
            {
              "$kind": "Microsoft.IfCondition",
              "$designer": {
                "id": "641773",
                "name": "Branch: if/else"
              },
              "condition": "string(dialog.foreach.value.id) != string(turn.Activity.Recipient.id)",
              "actions": [
                {
                  "$kind": "Microsoft.SendActivity",
                  "$designer": {
                    "id": "859266",
                    "name": "Send a response"
                  },
                  "activity": "${SendActivity_Welcome()}"
                }
              ]
            }
          ],
          "value": "dialog.foreach.value",
          "index": "dialog.foreach.index"
        }
      ]
    },
    {
      "$kind": "Microsoft.OnIntent",
      "$designer": {
        "id": "lCqUbV",
        "name": "MakeComplaint"
      },
      "intent": "MakeComplaint",
      "entities": [],
      "actions": [
        {
          "$kind": "Microsoft.BeginDialog",
          "$designer": {
            "id": "QprETM"
          },
          "activityProcessed": true,
          "dialog": "MakeComplaint"
        }
      ]
    },
    {
      "$kind": "Microsoft.OnIntent",
      "$designer": {
        "id": "EF0zn5",
        "name": "StatusofComplaint"
      },
      "intent": "StatusofComplaint",
      "actions": [
        {
          "$kind": "Microsoft.BeginDialog",
          "$designer": {
            "id": "ggTgYV"
          },
          "activityProcessed": true,
          "dialog": "StatusofComplaint"
        }
      ]
    },
    {
      "$kind": "Microsoft.OnIntent",
      "$designer": {
        "id": "8tccxX",
        "name": "FailureoftheMedicalApparatus"
      },
      "intent": "FailureoftheMedicalApparatus",
      "actions": [
        {
          "$kind": "Microsoft.BeginDialog",
          "$designer": {
            "id": "R7nf6Z"
          },
          "activityProcessed": true,
          "dialog": "FailureoftheIntrument"
        }
      ]
    },
    {
      "$kind": "Microsoft.OnIntent",
      "$designer": {
        "id": "73OTIU",
        "name": "TechnicalReview"
      },
      "intent": "TechnicalReview",
      "actions": [
        {
          "$kind": "Microsoft.BeginDialog",
          "$designer": {
            "id": "ZNBwSx"
          },
          "activityProcessed": true,
          "dialog": "TechnicalReview"
        }
      ]
    },
    {
      "$kind": "Microsoft.OnIntent",
      "$designer": {
        "id": "O0FiMO",
        "name": "PeripherialHardwareFailure"
      },
      "intent": "PeripherialHardwareFailure",
      "actions": [
        {
          "$kind": "Microsoft.BeginDialog",
          "$designer": {
            "id": "2fspbw"
          },
          "activityProcessed": true,
          "dialog": "PeripherialHardwareFailure"
        }
      ]
    },
    {
      "$kind": "Microsoft.OnIntent",
      "$designer": {
        "id": "P9m0dd",
        "name": "TakingPeripherialEquipment"
      },
      "intent": "TakingPeripherialEquipment",
      "actions": [
        {
          "$kind": "Microsoft.BeginDialog",
          "$designer": {
            "id": "utQGoY"
          },
          "activityProcessed": true,
          "dialog": "TakingPeripherialEquipment"
        }
      ]
    },
    {
      "$kind": "Microsoft.OnIntent",
      "$designer": {
        "id": "21j7ju",
        "name": "help"
      },
      "intent": "help",
      "actions": [
        {
          "$kind": "Microsoft.BeginDialog",
          "$designer": {
            "id": "Sa5m3g"
          },
          "activityProcessed": true,
          "dialog": "help"
        }
      ]
    }
  ],
  "$schema": "https://raw.githubusercontent.com/microsoft/BotFramework-Composer/stable/Composer/packages/server/schemas/sdk.schema",
  "generator": "RocMed.lg",
  "id": "RocMed",
  "recognizer": "RocMed.lu.qna"
}
