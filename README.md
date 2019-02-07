# Stardock

An evolution of [Starphleet](https://github.com/wballard/starphleet) backed by Docker containers

## Differences From Starphleet

- Containers are proper docker containers
  - Storage of containers no longer in S3.  Proper ECR / Repository support
- LXC subsystem for container management replaced by Docker
- Dependency on `upstart` removed
- Sessions
  - The url param for passing a session to Stardock is now "session=" rather than "jwt="
  - user_identity_cookie set by "un" claim allowing sessions to benefit from beta mechanisms traditionally only available to LDAP
- User key sync no longer bound to container publish
