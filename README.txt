Role-ként elkészítettem az Apache szerver feltelepítését, ami tartalmaz egy httpd daemon-t restartoló handler-t.
Viszont a DocumentRoot átírása rendes yaml file-ban történik meg alatta, mivel szintaktikai hibát nem tudtam megoldani, viszont teljesen jól lefut.
A mysql_install file-ban szintén található egy handler. Az SQL telepítését és konfigurálását nem mergeltem, szerintem így sokkal kezdő barátabb és átláthatóbb hogy mi történik.
Az SELinuxot nem sikerült működőképes állapotra hozni, így ezt kihagytam, a feladat leírásának megfelelően megváltozik a kért DocumentRoot nélküle is.
A 'chcon -R -t httpd_sys_content_t /opt/www'-t kellene futtatni, de mivel tanár úr kérte hogy a command modult ne használjuk, ezért ezt a megoldást a readme file-ba írom.
