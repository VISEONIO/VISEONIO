# VISEON Edge Integrity Prompt

## For AI Schema Creation:

**"Create Schema.org JSON-LD that passes the VISEON Edge Integrity Test. Ensure EVERY entity has bidirectional edge connections using these properties:**

**Required Edge Patterns:**
- `mainEntity` (WebPage → Thing) + `mainEntityOfPage` (Thing → WebPage)
- `hasPart` (Container → Thing) + `isPartOf` (Thing → Container)  
- `about` (CreativeWork → Thing) + `subjectOf` (Thing → CreativeWork)
- `provider/publisher` (Thing → Organization) for authority
- `sameAs` (Thing → External URL) for identity disambiguation

**Validation Rules:**
1. ✅ Every entity has unique `@id` with fragment identifier
2. ✅ All entities connect via at least ONE edge property
3. ✅ No orphaned entities floating without connections
4. ✅ Bidirectional relationships are complete (A→B requires B→A)
5. ✅ All references resolve within the @graph

**Test:** Can you traverse from any entity to any other entity through the edge relationships? If not, add the missing connections.**

---

*Based on [VISEON.IO](https://VISEON.IO) Edge Architecture principles for AI-discoverable knowledge graphs.*"
