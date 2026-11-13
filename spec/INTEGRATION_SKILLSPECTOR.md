# HEIMEL integration note: NVIDIA SkillSpector

This is a **non-normative** integration note. It does not change HEIMEL-CONFORMANCE/2.0, the 79 REQUIRED vectors, the immutable v0.2.0 release, or public reference-authority behavior.

NVIDIA SkillSpector may provide pre-install, content-bound security observations for agent skills and MCP packages. A scan is not a permit, an authority claim, a proof of behavior, or a certification. SkillSpector's SAFE recommendation is an input to component admission review only.

The external integrator should bind a scan result to an exact source digest and scanner version, maintain its own trusted source registry and install approval, reject stale or mismatched results, and retain tenant isolation. The report is untrusted input, even when the scanner exited zero.

For effectful actions the HEIMEL boundary remains authoritative: fresh authority at consequence time, actor/tenant/delegation confinement, exact effect binding, single-use semantics, fail-closed missing inputs and replayable evidence. The scanner must never add an ALLOW path or bypass a consequence boundary. Observation and receipt generation remain separate from authority.

This note intentionally does not prescribe a SkillSpector dependency for the public HEIMEL reference adapter.

Upstream: https://github.com/NVIDIA/SkillSpector (Apache-2.0).
