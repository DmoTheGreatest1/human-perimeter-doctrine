flowchart TB
  subgraph NIST["External Reference Frameworks"]
    EO["Executive Order 13636\n(Policy driver & CI cyber posture)"]
    CSF["NIST CSF 2.0\n(Governance & risk comms taxonomy)"]
    RA["NIST SP 800-30\n(Risk assessment method)"]
  end

  subgraph CCSM["CCSM (Constitutional Security Model)\nMeta-governance / constraint logic"]
    M["Constitutional Modules\n(M1–M10)"]
  end

  subgraph HPD["HPD (Human Perimeter Doctrine)\nGovernance recommendations / procedures"]
    G["Perimeter Rules + Custody + Human Authority\n(Ring-0, artifact handling, audit posture)"]
  end

  subgraph CAP["California Pilot\nField demonstration / exhibits"]
    E["Observed gaps + redacted artifacts + correspondence\n(non-enforcing)"]
  end

  EO --> CSF
  RA --> CSF

  CCSM --> HPD
  HPD --> CAP

  CSF -.maps to.- CCSM
  CSF -.maps to.- HPD
  CSF -.maps to.- CAP

  RA -.supports risk framing of.- CCSM
  RA -.supports risk framing of.- HPD
  RA -.supports risk framing of.- CAP
