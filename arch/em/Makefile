# ==========================================================================
# Build system
# ==========================================================================

SKIP_STRIP=y

cmd_busybox__ = \
      $(CC) \
      -o $@.js \
      --memory-init-file 0 \
      $(CFLAGS_busybox) \
      $(LDFLAGS) \
      $(EXTRA_LDFLAGS) \
      -Wl,--start-group \
      $(core-y) \
      $(libs-y) \
      $(patsubst %,-l%,$(subst :, ,$(LDLIBS))) \
      -Wl,--end-group \
      && mv $@.js $@
