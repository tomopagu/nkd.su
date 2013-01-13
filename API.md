## Endpoints

The root of the API is [nkd.su/api/][api_root]. The following endpoints are
available:

### [`/`][api_root]

Information about the week in progress. Includes:

- `votes`: a list of votes placed
- `playlist`: a list of tracks played and the times at which they were played
- `added`: a list of all the tracks added to the library this week
- `start`: the date and time at which this week started
- `finish`: the date and time at which this week ended 
- `showtime`: the date and time at which this week's show began

### [`/track/<track_id>/`][eg_track]

Information about a particular track, including metadata and a list of every
play on record.

Note that the `plays` list is only included for tracks in calls to
`/track/<track_id>`; tracks returned as part of other endpojnts will not have
`plays` listed.

### [`/week/<dd>-<mm>-<yyyy>/`][eg_week]

Information from a particular week, in the same format as that returned by
[`/`][api_root]. The week returned will be the week that was in progress at
midnight on the morning of the day specified.

### [`/week/`][eg_latest_week]

A redirect to the week containing the most recent complete show.

## More things

If there is something else you want added or changed, or if you find something
that's broken, [let me know][new_issue]. If you just have a question,
[tweet][pester] at me.

[new_issue]: https://github.com/colons/nkdsu/issues/new
[api_root]: http://nkd.su/api/
[eg_track]: http://nkd.su/api/track/7C4D7B4B394E0E59/
[eg_latest_week]: http://nkd.su/api/week/
[eg_week]: http://nkd.su/api/week/12-01-2013/
[pester]: https://twitter.com/intent/tweet?text=%40mftb