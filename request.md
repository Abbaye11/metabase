[
  { "$project": { "ActualVolume": 1, "MaxVolume": 1, "DateExport": 1,"ActualVolumePerCent":1, "CiterneTemperatureF":1 } },
  { "$limit": 500 }
]

[
  { "$project": { "ActualVolume": 1, "MaxVolume": 1, "DateExport": 1,"ActualVolumePerCent":{ "$toInt": "$ActualVolumePerCent" }, "CiterneTemperatureF":{ "$toInt": "$CiterneTemperatureF" } } },
  { "$limit": 500 }
]
