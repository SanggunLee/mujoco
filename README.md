# MuJoCo Physics

**MuJoCo** stands for **Mu**lti-**Jo**int dynamics with **Co**ntact. It is a
general purpose physics engine that aims to facilitate research and development
in robotics, biomechanics, graphics and animation, machine learning, and other
areas which demand fast and accurate simulation of articulated structures
interacting with their environment. <br>

로봇 공학, 생체역학, 그래픽 및 애니메이션, 기계 학습 및 환경과 상호 작용하는 관절 구조의 빠르고
정확한 시뮬레이션을 요구하는 기타 분야의 연구 개발을 촉진하는 것을 목표로 하는 범용 물리학 엔진입니다.

DeepMind has acquired MuJoCo, and we are currently making preparations to open
source the codebase. In the meantime, MuJoCo is available for download as a free
and unrestricted precompiled binary under the Apache 2.0 license from
[mujoco.org](https://mujoco.org/). <br>

DeepMind는 MuJoCo를 인수했고, 우리는 현재 코드베이스를 오픈소스로 준비하고 있다.<br>
그동안 MuJoCo는 mujoco.org의 Apache 2.0 라이센스에 따라 무료 및 무제한 사전 컴파일 바이너리로 다운로드할 수 있습니다.<br>

MuJoCo's source code will be released through this GitHub repository once it is
ready. In the meantime, the repository hosts MuJoCo's documentation, C header
files for its public API, and sample program code. If you wish to report bugs or
make feature requests, please file them as [GitHub Issues]. You are also
welcome to make pull requests for the [documentation source files].<br>

MuJoCo의 소스 코드는 준비가 되면 이 GitHub 저장소를 통해 공개될 것이다.<br>
그동안 저장소는 MuJoCo의 문서, 공개 API를 위한 C 헤더 파일 및 샘플 프로그램 코드를 호스팅합니다.<br> 
버그를 보고하거나 기능 요청을 하려면 GitHub Issues로 제출하십시오. 문서 소스 파일에 대한 풀 리퀘스트를 할 수도 있습니다.<br>



## Overview

MuJoCo is a C/C++ library with a C API, intended for researchers and developers.
The runtime simulation module is tuned to maximize performance and operates on
low-level data structures which are preallocated by the built-in XML parser and
compiler. The user defines models in the native MJCF scene description language
-- an XML file format designed to be as human readable and editable as possible.
URDF model files can also be loaded. The library includes interactive
visualization with a native GUI, rendered in OpenGL. MuJoCo further exposes a
large number of utility functions for computing physics-related quantities, not
necessarily in a simulation loop. Features include

MuJoCo는 연구원과 개발자를 위한 C API를 갖춘 C/C++ 라이브러리이다.
런타임 시뮬레이션 모듈은 성능을 극대화하기 위해 튜닝되며 내장 XML 파서와 컴파일러에 의해 사전 할당된 low-level 데이터 구조에서 작동합니다.
사용자는 네이티브 MJCF Scene descriptinon 언어(XML 파일 형식, 사람이 읽을 수 있고 편집할 수 있도록 설계)로 모델을 정의합니다. 
URDF 모델 파일도 로드할 수 있습니다.
library는 OpenGL로 렌더링된 네이티브 GUI와의 대화식 시각화를 포함한다.
MuJoCo는 물리학 관련 quantities 을 계산하기 위한 많은 유틸리티 기능을 노출한다, 시뮬레이션 루프에서 반드시 있는 것은 아니지만.
특징은 다음과 같습니다.


-   Simulation in generalized coordinates, avoiding joint violations.

-   Inverse dynamics that are well-defined even in the presence of contacts.

-   Unified continuous-time formulation of constraints via convex optimization.

-   Constraints include soft contacts, limits, dry friction, equality
    constraints.

-   Simulation of particle systems, cloth, rope and soft objects.

-   Actuators including motors, cylinders, muscles, tendons, slider-cranks.

-   Choice of [Newton, Conjugate Gradient, Projected Gauss-Seidel solvers]. <br>
    Conjugate Gradient : https://en.wikipedia.org/wiki/Conjugate_gradient_method<br>
    Gauss-Seidel solvers : https://ko.wikipedia.org/wiki/가우스-자이델_방법<br>
    The projected Gauss-Seidel (PGS) method is an extension of Gauss-Seidel used to solve MLCP's ...
    

-   Choice of pyramidal or elliptic friction cones, dense or sparse Jacobians.

-   Choice of Euler or Runge-Kutta numerical integrators.

-   Multi-threaded sampling and finite-difference approximations.

-   Intuitive XML model format (called MJCF) and built-in model compiler.

-   Cross-platform GUI with interactive 3D visualization in OpenGL.

-   Run-time module written in ANSI C and hand-tuned for performance.


## Requirements

MuJoCo binaries are currently built for Linux, macOS (Intel), and Windows.


## Documentation

MuJoco's current documentation is available at [mujoco.org/book], which is
serving Sphinx-based webpages derived from the ReStructuredText
[documentation source files].


## Citation

If you use MuJoCo for published research, please cite:

```
@inproceedings{todorov2012mujoco,
  title={Mujoco: A physics engine for model-based control},
  author={Todorov, Emanuel and Erez, Tom and Tassa, Yuval},
  booktitle={2012 IEEE/RSJ International Conference on Intelligent Robots and Systems},
  pages={5026--5033},
  year={2012},
  organization={IEEE}
}
```


## License and Disclaimer

Copyright 2021 DeepMind Technologies Limited

ReStructuredText documents, images, and videos in the `doc` directory are made
available under the terms of the Creative Commons Attribution 4.0 (CC BY 4.0)
license. You may obtain a copy of the License at
https://creativecommons.org/licenses/by/4.0/legalcode.

Source code is licensed under the Apache License, Version 2.0. You may obtain a
copy of the License at https://www.apache.org/licenses/LICENSE-2.0.

This is not an officially supported Google product.


[GitHub Issues]: https://github.com/deepmind/mujoco/issues
[documentation source files]: https://github.com/deepmind/mujoco/tree/main/doc
[mujoco.org/book]: https://mujoco.org/book

