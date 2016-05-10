cpack-deb-imporvements
----------------------

* The "CPackDeb" module learned how to generate DEBIAN/shlibs contorl file
  when package contains shared libraries.

* The "CPackDeb" module learned how to generate DEBIAN/postinst and
  DEBIAN/postrm files if package installs libraries in ldconfig controlled
  location (/lib/, /usr/lib/).

* The "CPackDeb" module learned how to generate dependencies between Debian
  packages if multi-component setup is used and :variable:`CPACK_COMPONENT_<compName>_DEPENDS`
  variables are set (breaks compatibility with previous versions).

* The "CPackDeb" module learned how to set package release number
  (DebianRevisionNumber in package file name). See :variable:`CPACK_DEBIAN_PACKAGE_RELEASE`.

* The "CPackDeb" module learned how to generate proper debian package names
  with format ``<PackageName>_<VersionNumber>-<DebianRevisionNumber>_<DebianArchitecture>.deb``
  (breaks compatibility with previous versions).

* The "CPackDeb" module learned how to set package architecture per-component.
  See :variable:`CPACK_DEBIAN_<COMPONENT>_PACKAGE_ARCHITECTURE`.
