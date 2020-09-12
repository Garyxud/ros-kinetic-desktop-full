^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package collada_urdf
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.12.13 (2020-07-14)
--------------------
* Update to newer CMake to get rid of CMP0048 warning (`#38 <https://github.com/ros/collada_urdf/issues/38>`_)
* Enable to output transmission_interface instead of pr2_mechanism_model (`#35 <https://github.com/ros/collada_urdf/issues/35>`_)
* Contributors: Chris Lalancette, Shun Hasegawa

1.12.12 (2018-05-08)
--------------------

1.12.11 (2018-04-17)
--------------------
* Collada cleanup dependencies (`#26 <https://github.com/ros/collada_urdf/issues/26>`_)
* update links now that this is in its own repo
* Switch to using Eigen for Quaternion and Matrix. (`#21 <https://github.com/ros/collada_urdf/issues/21>`_)
* add relicensing comment (`#19 <https://github.com/ros/collada_urdf/issues/19>`_)
* remove unused tinyxml from cmakelists (`#15 <https://github.com/ros/collada_urdf/issues/15>`_)
* Contributors: Chris Lalancette, Mikael Arguedas, Rosen Diankov

1.12.10 (2017-05-04)
--------------------
* Moved collada_parser and collada_urdf to new repository

1.12.9 (2017-04-26)
-------------------

1.12.8 (2017-03-27)
-------------------
* Remove old gazebo settings.
  Based on an initial patch from YoheiKakiuchi, just totally
  remove old Gazebo 1.0 settings, as they are never used and
  almost certainly will never be used.
* add Chris and Shane as maintainers (`#184 <https://github.com/ros/robot_model/issues/184>`_)
* Do a few cleanup tasks in collada_urdf (`#183 <https://github.com/ros/robot_model/issues/183>`_)
  * Style cleanup within collada_urdf.
  No functional change, just style.
  * Make sure to quit out of urdf_to_collada when invalid file is found.
  Otherwise, we'll just end up segfaulting later on.
  * Re-enable one of the collada-urdf tests.
  In point of fact, we delete the rest of the tests because
  they don't make much sense anymore.  Just enable this one
  for now; we'll enable further ones in the future.
  * Add in another test for collada_urdf.
* remove divide by 2 when writing boxes to collada format (`#133 <https://github.com/ros/robot_model/issues/133>`_)
* Contributors: Chris Lalancette, Jackie Kay, William Woodall

1.12.7 (2017-01-26)
-------------------

1.12.6 (2017-01-04)
-------------------
* Now using ``urdf::*ShredPtr`` instead of ``boost::shared_ptr`` (`#144 <https://github.com/ros/robot_model/issues/144>`_)
* Contributors: Jochen Sprickerhof

1.12.5 (2016-10-27)
-------------------

1.12.4 (2016-08-23)
-------------------
* Use the C++11 standard (`#145 <https://github.com/ros/robot_model/issues/145>`_)
* Contributors: William Woodall

1.12.3 (2016-06-10)
-------------------

1.12.2 (2016-04-12)
-------------------

1.12.1 (2016-04-10)
-------------------

1.11.8 (2015-09-11)
-------------------
* Removed pcre hack for newer released collada-dom.
* Contributors: Kei Okada

1.11.7 (2015-04-22)
-------------------
* Fixed `#89 <https://github.com/ros/robot_model/issues/89>`_
  Accomplished by loading libpcrecpp before collada-dom.
* Contributors: Kei Okada, William Woodall

1.11.6 (2014-11-30)
-------------------

1.11.5 (2014-07-24)
-------------------

1.11.4 (2014-07-07)
-------------------
* moving to new dependency for urdfdom and urdfdom_headers. https://github.com/ros/rosdistro/issues/4633
* Fix clash with assimp 3.1 in CMake.
* Contributors: Benjamin Chrétien, Tully Foote

1.11.3 (2014-06-24)
-------------------
* Merge pull request `#69 <https://github.com/ros/robot_model/issues/69>`_ from YoheiKakiuchi/indigo-devel-store-original-mesh-name
  storing original mesh file name and location
* storing original mesh file name and location
* Contributors: Ioan A Sucan, YoheiKakiuchi

1.11.2 (2014-03-22)
-------------------
* use new  urdfdom_headers API
* Contributors: Ioan Sucan

1.11.1 (2014-03-20)
-------------------
* Use assimp-dev dep for building
* Contributors: Scott K Logan

1.11.0 (2014-02-21)
-------------------
* Use VERSION_LESS instead of STRLESS
  The version comparison routines were added in cmake 2.8.0
* Fix export API detection (for assimp < 2.0.885)
  It looks like this API was added in Assimp 2.0.885:
  https://github.com/assimp/assimp/commit/ae23c03bd9a0b5f1227dc0042fd98f7206c770a8
* Invert Assimp version detect logic for greater accuracy
* Updated Assimp defines to be more flexible
  This commit is a follow-up to 85b20197671e142044e471df603debd0faf08baf
  Why was export.h removed from assimp < 3.0.0?
* Better feature detection for assimp version
  The unified headers were introduced in Assimp 2.0.1150, so checking for Assimp 3.0.0 is not quite the best solution.
  See https://github.com/assimp/assimp/commit/6fa251c2f2e7a142bb861227dce0c26362927fbc
* Contributors: Scott K Logan

1.10.18 (2013-12-04)
--------------------
* add DEPENDS for kdl_parser
* Contributors: Ioan Sucan

1.10.16 (2013-11-18)
--------------------
* check for CATKIN_ENABLE_TESTING
* fix for compiling collada_to_urdf, add dependency to tf
* add collada_to_urdf.cpp for converting collada file to urdf file

1.10.15 (2013-08-17)
--------------------
* fix `#30 <https://github.com/ros/robot_model/issues/30>`_
