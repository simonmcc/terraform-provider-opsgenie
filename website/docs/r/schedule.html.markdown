---
layout: "opsgenie"
page_title: "Opsgenie: opsgenie_schedule"
sidebar_current: "docs-opsgenie-resource-schedule"
description: |-
  Manages a Schedule within Opsgenie.
---

# opsgenie_schedule

Manages a Schedule within Opsgenie.

## Example Usage
```hcl
resource "opsgenie_schedule" "test" {
  name = "genieschedule-%s"
  description = "schedule test"
  timezone = "Europe/Rome"
  enabled = false
}
```
```hcl
resource "opsgenie_schedule" "test" {
  name = "genieschedule-%s"
  description = "schedule test"
  timezone = "Europe/Rome"
  enabled = false
  owner_team_id = "${opsgenie_team.test.id}"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) Name of the schedule.

* `rules` - (Required) A Member block as documented below.

* `description` - (Optional) Timezone of schedule. Please look at [Supported Timezone Ids](https://docs.opsgenie.com/docs/supported-timezone-ids) for available timezones - Defaults to "America/New_York".

* `timezone` - (Optional) The description of schedule.

* `enabled` - (Optional) Enable/disable state of schedule

* `owner_team_id` - (Optional) Owner team id of the schedule.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the Opsgenie Schedule.

## Import

Schedule can be imported using the `id`, e.g.

```
$ terraform import opsgenie_schedule.test 812be1a1-32c8-4666-a7fb-03ecc385106c
```
