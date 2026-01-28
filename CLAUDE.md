# Water Damage Restoration Landing Page

Pay-per-call landing page for water damage restoration services.

---

## Project Status: LIVE

**Live URL:** https://water-damage-helpline.com
**GitHub:** https://github.com/justingumpglobal/water-damage-helpline-landing
**Deployment:** Cloudflare Pages (auto-deploy from GitHub)

---

## Quick Reference

**Phone:** (833) 648-3507
**Ringba Campaign ID:** CA0a0649f7e6cf4526a9d19b4fd3b37037
**Supabase Project:** rpcoelumfrzvbwnhvmnp

### Run Commands
```bash
# Test locally
python -m http.server 8000

# Push changes (auto-deploys via GitHub)
git add . && git commit -m "message" && git push
```

---

## Database Tables

| Table | Rows | Description |
|-------|------|-------------|
| `restoration_services` | 23 | All service types with slugs, categories |
| `restoration_service_content` | 23 | Headlines, CTAs, common problems per service |
| `restoration_testimonials` | 69 | 3 per service, emotional/natural style |
| `restoration_insurance_providers` | 7 | State Farm, Allstate, Progressive, Liberty Mutual, Farmers, USAA, Nationwide |

### RPC Function
- `get_restoration_content(p_service_slug)` - Returns all dynamic content for a service

---

## Services (23 total)

### Water Damage (10)
| Slug | Name |
|------|------|
| water-damage-restoration | Water Damage Restoration |
| water-extraction | Water Extraction |
| flood-cleanup | Flood Cleanup |
| basement-flooding | Basement Flooding |
| burst-pipe-cleanup | Burst Pipe Cleanup |
| appliance-water-damage | Appliance Water Damage |
| storm-damage | Storm Damage |
| sewage-cleanup | Sewage Cleanup |
| structural-drying | Structural Drying |
| emergency-water-removal | Emergency Water Removal |

### Mold (4)
| Slug | Name |
|------|------|
| mold-remediation | Mold Remediation |
| mold-removal | Mold Removal |
| mold-inspection | Mold Inspection |
| black-mold-removal | Black Mold Removal |

### Fire/Smoke (4)
| Slug | Name |
|------|------|
| fire-damage-restoration | Fire Damage Restoration |
| smoke-damage-cleanup | Smoke Damage Cleanup |
| odor-removal | Odor Removal |
| soot-cleanup | Soot Cleanup |

### Specialty (5)
| Slug | Name |
|------|------|
| contents-restoration | Contents Restoration |
| biohazard-cleanup | Biohazard Cleanup |
| carpet-water-damage | Carpet Water Damage |
| ceiling-water-damage | Ceiling Water Damage |
| crawl-space-water-damage | Crawl Space Water Damage |

---

## URL Parameters

| Parameter | Example | Description |
|-----------|---------|-------------|
| `service` | `?service=mold-remediation` | Loads service-specific content |
| `loc_physical_ms` | `?loc_physical_ms=9003499` | Google Ads geo-targeting code |

**Full URL Example:**
```
https://water-damage-helpline.com/?service=water-damage-restoration&loc_physical_ms=9003499
```

---

## File Structure

```
water-damage/
├── CLAUDE.md                  # This file
├── index.html                 # Main landing page
├── privacy.html               # Privacy policy
├── terms.html                 # Terms of service
├── current_ad_groups.txt      # Tracking created ad groups
├── ad-exports/
│   └── templates/
│       └── ad-group-template.csv
└── assets/
    └── images/
        ├── hero/              # Hero section images
        ├── process/           # 3-step process images
        ├── services/          # Service card images
        └── insurance/         # Insurance provider logos
```

---

## Post-Launch TODO

- [ ] Verify Ringba phone swap works on live domain
- [ ] Mobile test on real devices
- [ ] Set up Google Ads campaigns
- [ ] Inquirly compliance check on "60-minute response" claim (if needed)
