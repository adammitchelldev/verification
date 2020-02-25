#
# GRAKN.AI - THE KNOWLEDGE GRAPH
# Copyright (C) 2019 Grakn Labs Ltd
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU Affero General Public License as
# published by the Free Software Foundation, either version 3 of the
# License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU Affero General Public License for more details.
#
# You should have received a copy of the GNU Affero General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.
#

package(default_visibility = ["//visibility:public"])

load("@graknlabs_build_tools//checkstyle:rules.bzl", "checkstyle_test")

java_test(
    name = "semantic-set-validity",
    srcs = glob([
        "SemanticSets.java",
    ]),
    test_class = "grakn.verification.tools.integrity.test.SemanticSets",
    deps = [
        "//tools/integrity:integrity",
        "@graknlabs_client_java//:client-java",
        "@graknlabs_graql//java:graql",
        "@graknlabs_common//:common",
        "//dependencies/maven/artifacts/com/google/guava",
        "//dependencies/maven/artifacts/org/mockito:mockito-core",
    ],

)

checkstyle_test(
    name = "checkstyle",
    targets = [
        ":semantic-set-validity",
    ],
)