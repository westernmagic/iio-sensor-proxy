udevrules_DATA = 80-iio-sensor-proxy.rules

systemdservicedir = $(systemdsystemunitdir)
systemdservice_in_files = iio-sensor-proxy.service.in
systemdservice_DATA = iio-sensor-proxy.service
iio-sensor-proxy.service: iio-sensor-proxy.service.in Makefile
	$(AM_V_GEN) $(SED) -e "s|\@sbindir\@|$(sbindir)|" $< > $@

dbusconfdir = $(sysconfdir)/dbus-1/system.d
dbusconf_DATA = net.hadess.SensorProxy.conf

CLEANFILES = iio-sensor-proxy.service
EXTRA_DIST = $(udevrules_DATA) $(dbusconf_DATA) $(systemdservice_in_files)
