# Copyright 2016 The Kubernetes Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

ARG BASE_IMAGE=microsoft/windowsservercore:1803
FROM $BASE_IMAGE

ENV LOGS_GENERATOR_LINES_TOTAL 1
ENV LOGS_GENERATOR_DURATION 1s

COPY logs_generator.exe /

CMD ["powershell", "/logs_generator.exe --logtostderr --log-lines-total=$env:LOGS_GENERATOR_LINES_TOTAL --run-duration=$env:LOGS_GENERATOR_DURATION"]
