# spgateway_payment_and_invoice

Legacy gem. Still used by production Rails apps. Keep changes minimal.

## Toolchain

- `bundle install` works on Ruby 4.0.9 with Bundler 4.
- `bundle exec rake` fails on Ruby 4: rake 12.3 needs `ostruct`, which Ruby 4 no longer ships.

## Checks

- There are no tests. Verify a change loads with `bundle exec ruby -Ilib -e 'require "spgateway"'`.

## Consumers

- Apps install this gem from GitHub `branch: 'master'` and pin a `revision:` in Gemfile.lock. A push to master reaches no app until that app runs `bundle update spgateway_payment_and_invoice_client`.
