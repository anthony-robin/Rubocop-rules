# Rubocop rules

This project contains the default rubocop rules that can be applied
to every projects.

## Getting started

```yaml
inherit_from: https://raw.githubusercontent.com/anthony-robin/rubocop-rules/master/.rubocop.yml
```

In some case, you might want to override rules: no problem! Just add your new rule **AFTER** the `inherit_from` line:

```yaml
inherit_from: https://raw.githubusercontent.com/anthony-robin/rubocop-rules/master/.rubocop.yml

Rails/Date:
  Enabled: false

# Other rules
```

## Notes

- When using `inherit_from`, Rubocop will fetch and download the remote file on the root of your project. You don't want to track this file with git so add it to your `.gitignore`:
  ```
    .rubocop-http*
  ```

- As Ruby version might be different between projects, ensure you have set the following line with the Ruby version used in your project:
  ```yaml
  AllCops:
    TargetRubyVersion: 2.4
  ```

# Related links
- https://github.com/bbatsov/rubocop/blob/master/manual/configuration.md#inheriting-configuration-from-a-remote-url
