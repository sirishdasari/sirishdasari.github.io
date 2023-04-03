---
slug: "cheatcode-arcpy"
date: "2023-01-01"
title: "Arcpy"
tags: ["cheat codes"]
description: "This is a quick reference for Arcpy library" 
---
## Cursors
```python
# Search Cursor
with arcpy.da.SearchCursor("Feature","Fields") as cursor:
	for row in cursor:
		print(row)

# Update Cursor
with arcpy.da.UpdateCursor("Feature","Fields") as cursor:
	for row in cursor:
		row[0] = "Assign"
		cursor.updateRow(row)
		
# Insert Cursor
with arcpy.da.InsertCursor("Feature","Fields") as cursor:
	for row in cursor:
		cursor.insertRow(("Assign"))
```
