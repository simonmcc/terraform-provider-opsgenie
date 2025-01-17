---
layout: "opsgenie"
page_title: "Opsgenie: opsgenie_user"
sidebar_current: "docs-opsgenie-resource-user"
description: |-
  Manages a User within Opsgenie.
---

# opsgenie\_user

Manages a User within Opsgenie.

## Example Usage

```hcl
resource "opsgenie_user" "test" {
  username  = "user@domain.com"
  full_name = "Cookie Monster"
  role      = "User"
  locale    = "en_US"
  timezone  = "America/New_York"
}
```

## Argument Reference

The following arguments are supported:

* `username` - (Required) The email address associated with this user. Opsgenie defines that this must not be longer than 100 characters.

* `full_name` - (Required) The Full Name of the User.

* `role` - (Required) The Role assigned to the User. Either a built-in such as 'Owner', 'Admin' or 'User' - or the name of a custom role.

* `locale` - (Optional) Location information for the user. Please look at [Supported Locale Ids](https://docs.opsgenie.com/docs/supported-locales) for available locales.

* `timezone` - (Optional) Timezone information of the user. Please look at [Supported Timezone Ids](https://docs.opsgenie.com/docs/supported-timezone-ids) for available timezones.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the Opsgenie User.

## Import

Users can be imported using the `id`, e.g.

```
$ terraform import opsgenie_user.user da4faf16-5546-41e4-8330-4d0002b74048
```
