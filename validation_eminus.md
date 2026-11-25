# Yields: pyCount, RooCount, Shape on MDS4b_CeMLeadingLog_1e-13_pe1 (minus)

**Verdict: PASS**

| check | status | detail |
|---|---|---|
| cutflow pyCount = RooCount | PASS | 23 cuts compared; cuts in only one: signal_region |
| selected tracks pyCount = RooCount | PASS | 219 in both, 0 only pyCount, 0 only RooCount; max |dp| 0 MeV/c, max |dt| 0 ns |
| MC labels agree | PASS | all labels agree |
| tracks in fit range RooCount = Shape | PASS | 219 in both, 0 only RooCount, 0 only Shape |
| Shape fit converged | PASS | status 0, covQual 3 |
| Shape yields within 3 sigma of MC truth | PASS | CE -0.9, DIO -0.4, Cosmic +0.5, RPC +1.1, RMC +0.2 |
| pyCount run provenance | PASS | /exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1 at commit 093973e7 |

Files: `/exp/mu2e/data/users/mu2epro/ensembles/MDS4/MDS4b/signal/CeMLeadingLog_1e-13/pe_1/mixed_files.txt` (8 files). Selection: pyCount profile `nominal_minus`, C++ cut version `run1a`. Raw MC counts of this pseudo-experiment, tracks (not events).

## selected: p in (100.0, 110.0) MeV/c, t in (475.0, 1650.0) ns

| process | pyCount | RooCount |
|---|---|---|
| CE | 73 | 73 |
| DIO | 49 | 49 |
| RPC | 42 | 42 |
| RMC | 2 | 2 |
| Cosmic | 53 | 53 |
| total | 219 | 219 |

## signal_window: p in (103.34, 104.74) MeV/c, t in (640.0, 1650.0) ns

| process | pyCount | RooCount | Shape (MC truth) |
|---|---|---|---|
| CE | 42 | 42 | 42 |
| Cosmic | 2 | 2 | 2 |
| total | 44 | 44 | 44 |

## fit_range: p in (100.0, 110.0) MeV/c, t in (475.0, 1650.0) ns

| process | pyCount | RooCount | Shape (MC truth) |
|---|---|---|---|
| CE | 73 | 73 | 73 |
| DIO | 49 | 49 | 49 |
| RPC | 42 | 42 | 42 |
| RMC | 2 | 2 | 2 |
| Cosmic | 53 | 53 | 53 |
| total | 219 | 219 | 219 |

## Shape 2D fit vs MC truth (RooCount labels)

Fit status 0, covQual 3, EDM 0.00069, significance 7.81 sigma. Values at the signal+background minimum; signal window = fitted yield x fraction of the fitted component inside the window.

| component | processes | fit (fit range) | MC (fit range) | fit (signal window) | MC (signal window) |
|---|---|---|---|---|---|
| CE | CE | 63.18 ± 10.38 | 73 | 34.86 ± 5.73 | 42 |
| DIO | DIO | 41.90 ± 17.04 | 49 | 0.01 ± 0.01 | 0 |
| Cosmic | Cosmic | 58.13 ± 11.01 | 53 | 7.57 ± 1.43 | 2 |
| RPC | RPC | 50.89 ± 7.87 | 42 | 0.00 ± 0.00 | 0 |
| RMC | RMC | 4.87 ± 13.10 | 2 | 0.00 ± 0.00 | 0 |
| not modelled | CEP+IPA+FlatEminus+FlatEplus+Other | - | 0 | - | 0 |

## Cut flow (events)

| cut | pyCount | RooCount |  |
|---|---|---|---|
| all_events | 1272050 | 1272050 |  |
| has_a_track | 661053 | 661053 |  |
| is_good_track | 659080 | 659080 |  |
| has_trk_front_seg | 641167 | 641167 |  |
| is_reco_electron_or_positron | 620836 | 620836 |  |
| has_downstream | 586925 | 586925 |  |
| charge_selection | 385896 | 385896 |  |
| or_trigger | 208145 | 208145 |  |
| upstream_veto | 192146 | 192146 |  |
| no_multi_trk_veto | 174529 | 174529 |  |
| good_trkpid | 100183 | 100183 |  |
| pz_over_pt | 71147 | 71147 |  |
| within_d0 | 67680 | 67680 |  |
| st_boundary | 66843 | 66843 |  |
| has_st | 64213 | 64213 |  |
| no_opa | 63874 | 63874 |  |
| no_tsda | 63688 | 63688 |  |
| good_trkqual | 54479 | 54479 |  |
| has_hits | 54228 | 54228 |  |
| within_t0err | 54228 | 54228 |  |
| no_crv_veto | 53952 | 53952 |  |
| in_mom_range | 543 | 543 |  |
| within_t0_475 | 219 | 219 |  |
| signal_region |  | 44 | **differs** |

## Track by track

- pyCount_vs_RooCount: both 219, only_pyCount 0, only_RooCount 0, label_differs 0, max_abs_dmom 0, max_abs_dtime 0
- RooCount_vs_Shape_fit_range: both 219, only_RooCount 0, only_Shape 0, label_differs 0

## Provenance

```
{
 "tag": "MDS4b_CeMLeadingLog_1e-13_pe1",
 "sign": "minus",
 "profile": "nominal_minus",
 "version": "run1a",
 "fit_window": [
  100.0,
  110.0,
  475.0,
  1650.0
 ],
 "file_list": "/exp/mu2e/data/users/mu2epro/ensembles/MDS4/MDS4b/signal/CeMLeadingLog_1e-13/pe_1/mixed_files.txt",
 "file_list_sha256": "94700207f09435dab296a17caedf10f635f400ae35e439b28a04c030abe12eb3",
 "n_files": 8,
 "pycount_run": "/exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1",
 "pycount_run_commit": "093973e7891828f3d46f0f9b51ce648dc61d656b",
 "pycount_run_dirty": false,
 "runs": {
  "pyCount": {
   "reused": true
  },
  "roocount": {
   "command": "source /cvmfs/mu2e.opensciencegrid.org/setupmu2e-art.sh && cd /exp/mu2e/app/users/sophie/newOffline && muse setup -q e29:p110 && cd /exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1/validation_eminus/roocount && RooCount /exp/mu2e/data/users/mu2epro/ensembles/MDS4/MDS4b/signal/CeMLeadingLog_1e-13/pe_1/mixed_files.txt /exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1/validation_eminus/roocount/roocount.root MDS4b_CeMLeadingLog_1e-13_pe1 run1a minus",
   "elapsed_s": 613.9
  },
  "shape": {
   "command": "source /cvmfs/mu2e.opensciencegrid.org/setupmu2e-art.sh && cd /exp/mu2e/app/users/sophie/newOffline && muse setup -q e29:p110 && cd /exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1/validation_eminus/shape && RefAnaShape /exp/mu2e/data/users/mu2epro/ensembles/MDS4/MDS4b/signal/CeMLeadingLog_1e-13/pe_1/mixed_files.txt MDS4b_CeMLeadingLog_1e-13_pe1 true 100.0 110.0 475.0 1650.0 2D run1a /exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1/validation_eminus/shape/shape.root",
   "elapsed_s": 615.2
  }
 },
 "commit": {
  "RefAna": "093973e",
  "EventNtuple": "0e07c92"
 },
 "user": "sophie",
 "host": "mu2egpvm05.fnal.gov",
 "started": "2026-11-25T08:26:19",
 "finished": "2026-11-25T08:36:36",
 "command": [
  "/exp/mu2e/app/users/sophie/newOffline/RefAna/compare/mds_yields.py",
  "/exp/mu2e/data/users/mu2epro/ensembles/MDS4/MDS4b/signal/CeMLeadingLog_1e-13/pe_1",
  "--sign",
  "minus",
  "--pycount-run",
  "/exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1",
  "--out",
  "/exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/runs/20261125-082255_refana_pe_1/validation_eminus"
 ]
}
```
