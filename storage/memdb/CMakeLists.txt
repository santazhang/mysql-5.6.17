# Copyright (c) 2006, 2010, Oracle and/or its affiliates. All rights reserved.
# 
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; version 2 of the License.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301 USA

SET(MEMDB_PLUGIN_STATIC "ha_memdb")

SET(MEMDB_SOURCES ha_memdb.cc
    base/basetypes.cc base/debugging.cc base/logging.cc base/misc.cc
    base/strop.cc base/threading.cc base/unittest.cc
    MurmurHash3.cc row.cc schema.cc table.cc
    txn.cc utils.cc value.cc xxhash.cc)
MYSQL_ADD_PLUGIN(memdb ${MEMDB_SOURCES} STORAGE_ENGINE MANDATORY)
