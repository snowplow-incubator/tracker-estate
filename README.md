# Snowplow Tracker Estate

**For internal reference.**

To see the tracker information, go here: [Snowplow Tracker Estate](https://snowplow-incubator.github.io/tracker-estate/) (Github Pages).

## How this repo works
The `all_properties` folder has files containing different tracker features or properties. Each one will make a different table.
The `tracker_details` folder has details for every tracker that match the features/properties in the table files.

For example, `features.md` has the line `Flush events command`. The tracker files also have this (exact wording!) line, plus whether or not it's present in the tracker, in the form `Flush events command | y`.

Annotations are added after a pipe separator. For example, `Flush events command | to flush events`, or `Flush events command | n | some explanation`.

A Ruby script reads all the files and generates the html.

### Updating details for a tracker
In the `tracker_details` folder, find the correct tracker file. Update the information as required. Commit to `main`. The Github Action will update the published html.
