# arch-pkgbuilds

## dkms-prune

Cleanup stale dkms modules

This adds a script + a oneshot service to cleanup stale dkms modules (i.e. not for an installed or running kernel.)

This is primarily useful if you use the `kernel-mdoules-hook` package so modules for the running kernel are preserved
when kernel updates ocurr so that reboots can be deferred.

That package does provide a service `linux-modules-cleanup.service` to cleanup old kernel modules, but it doesn't
affect dkms modules which is specifically what this deals with.
