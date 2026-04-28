# Data Dictionary

This document describes the three CSV files used in the Blondie Recipe Generator. These files contain the cleaned and processed recipe data that powers the ingredient calculator.

## df_pivot.csv
One row per recipe. Contains all ingredient amounts and derived ratios used for analysis.

| Column | Type | Description |
|---|---|---|
| Recipe_url | string | Source URL of the recipe |
| add_ins | float | Total weight of add-ins (chocolate chips, nuts, etc.) in grams |
| baking_powder | float | Baking powder amount in grams (standardised from baking soda where needed) |
| butter | float | Butter amount in grams |
| cornstarch | float | Cornstarch amount in grams |
| egg | float | Egg amount in grams (where provided) |
| flour | float | All-purpose flour amount in grams |
| salt | float | Salt amount in grams |
| sugar | float | Total sugar amount in grams |
| vanilla | float | Vanilla extract amount in grams/ml |
| butter_to_flour | float | Ratio of butter to flour |
| butter_to_sugar | float | Ratio of butter to sugar |
| sugar_to_flour | float | Ratio of sugar to flour |
| whole_eggs | int | Number of whole eggs used |
| egg_yolks | int | Number of additional egg yolks used |
| fat_ratio | float | Alias for butter_to_flour |
| sugar_ratio | float | Alias for sugar_to_flour |
| brown | float | Brown sugar amount in grams |
| white | float | White sugar amount in grams |
| brown_ratio | float | Brown sugar as a proportion of total sugar |
| white_ratio | float | White sugar as a proportion of total sugar |

## df_vanilla_ratios.csv
One row per recipe. Contains vanilla amounts and their ratio to flour, used to derive the vanilla_to_flour median for the generator.

| Column | Type | Description |
|---|---|---|
| Recipe_url | string | Source URL of the recipe |
| grams_converted | float | Vanilla extract amount in grams/ml |
| flour | float | Flour amount in grams for that recipe |
| vanilla_to_flour | float | Ratio of vanilla to flour |

## df_baking_powder_ratios.csv
One row per recipe. Contains baking powder amounts and their ratio to flour, used to derive the bp_to_flour median for the generator.

| Column | Type | Description |
|---|---|---|
| Recipe_url | string | Source URL of the recipe |
| grams_converted | float | Baking powder amount in grams |
| flour | float | Flour amount in grams for that recipe |
| bp_to_flour | float | Ratio of baking powder to flour |