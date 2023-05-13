# feeith

take a peek into someone else's ~~head~~ bluesky feed.

feeith lets you generate a feed that replicates the "following" tab for any
other bsky user.

## usage

feeds can be found at `feeith.nightmarl.in/{{@handle.bsky.social}}`. this may
change without notice in future.

## goals

- [ ] connect to bsky and start listening for skeets
- [ ] generate a feed
- [ ] filter skeets by user
- [ ] look up which users a user is "following"
- [ ] generate a feed that contains skeets from the users a user is following \[mvp\]
    - [ ] generate these feeds for multiple users
- [ ] auto-cleanup
    feeds are first generated when `//feith/{{@handle.bsky.social}}` is called,
    and are updated from that point onwards. if after $DURATION, a feed has not
    been viewed, remove it and any associated data
- [ ] backfill
- [ ] web ui & basic auth
    - [ ] log in with bsky handle and app pswd
    - [ ] generate a feed based on the given user
    - [ ] can't generate if blocked by that user
    - [ ] feeds can only be accessed with app passwords and if that user has succesfully generated a feed.
- [ ] privacy
    - [ ] skeet when a new feed is created (tagging that user)
        ```
        [automated message]
        hey @user.bsky.social, @user2.bsky.social has generated a feeith feed
        from your perspective. find out more at https://feeith.nightmarl.in/.
        ```
    - [ ] allow users to opt out (any skeet mentioning the bot containing the word "stop")
        ```
        reply 'stop' to this post to disable the feed.
        ```
    - [ ] allow users to create allowlists/blocklists
