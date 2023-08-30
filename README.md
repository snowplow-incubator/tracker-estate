# Snowplow Tracker Estate

**For internal reference.**

To see the tracker information, go here: [Snowplow Tracker Estate](https://snowplow-incubator.github.io/tracker-estate/) (Github Pages).

## How this repo works
The `all_properties` folder has files containing different tracker features or properties. Each one will make a different table.

The `tracker_details` folder has details for every tracker that match the features/properties in the table files.

For example, `features.md` has the line `Flush events command`. The tracker files also have this (exact wording!) line, plus whether or not it's present in the tracker, in the form `Flush events command | y`. A line can be present in multiple table files in `all_properties`, e.g. `Session pausable` is part of the general Features table as well as the Session table.

Annotations are added after a pipe separator. For example, `Flush events command | to flush events`, or `Flush events command | n | some explanation`.

A Ruby script reads all the files and generates the html.

### Updating details for a tracker
1. In the `tracker_details` folder, find the correct tracker file. 
2. Update the information as required. 
3. Run `ruby tracker_estate.rb` to update the html.
4. Commit to `main`.
