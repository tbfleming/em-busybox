# ==========================================================================
# Build system
# ==========================================================================

SKIP_STRIP=y

cmd_busybox__ = \
      $(CC) \
      -o $@.js \
      --memory-init-file 0 \
      -Wl,--start-group \
      $(CFLAGS) \
      $(CFLAGS_busybox) \
      $(LDFLAGS) \
      $(EM_LDFLAGS) \
      $(EXTRA_LDFLAGS) \
      $(core-y) \
      $(libs-y) \
      $(patsubst %,-l%,$(subst :, ,$(LDLIBS))) \
      -Wl,--end-group \
      && mv $@.js $@
