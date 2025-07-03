# Week 2 - Day 9: Database Design Workshop

## Daily Overview
**Theme:** Building Your Data Foundation
**Total Time:** 6-7 hours (1.5 instructor, 4.5-5.5 student)

## Hourly Schedule

### 9:00 AM - Data Thinking Warmup
**Duration:** 1 hour
**Type:** Self-paced

**Morning Data Assessment:**
- [ ] List all data your MVP will store
- [ ] Identify what users will create/read/update/delete
- [ ] Map data relationships
- [ ] Consider privacy requirements
- [ ] Note performance concerns

**Data Inventory Exercise:**
Write down:
1. **User Data:** Profiles, preferences, behavior
2. **Content Data:** Posts, files, messages
3. **System Data:** Settings, logs, analytics
4. **Relationship Data:** Connections, permissions

**Think About:**
- What data is public vs private?
- Which users can see what?
- How will data grow over time?
- What reports will you need?

---

### 10:00 AM - Live Session: Database Fundamentals
**Duration:** 1.5 hours
**Type:** Instructor-led

#### 10:00-10:15 AM: Database Mindset
**Instructor Activities:**
- Explain data importance
- Show bad database examples
- Discuss scalability early
- Set careful planning mindset

**Key Principles:**
- Plan twice, build once
- Privacy by design
- Performance matters
- Users first

#### 10:15-10:45 AM: Data Types & Relationships
**Instructor Activities:**
- Explain different data types
- Show relationship examples
- Demonstrate Bubble data tab
- Build simple data model live

**Bubble Data Types:**
- **Text:** Names, descriptions
- **Number:** Prices, counts, ratings
- **Date:** Created times, schedules
- **Yes/No:** Flags, permissions
- **File:** Images, documents
- **User:** Built-in user type
- **Geographic Address:** Locations

**Relationship Types:**
- **One-to-Many:** User → Posts
- **Many-to-Many:** Users ↔ Groups
- **One-to-One:** User → Profile

#### 10:45-11:15 AM: Privacy Rules Deep Dive
**Instructor Activities:**
- Explain privacy importance
- Show rule creation
- Demonstrate testing
- Discuss common mistakes

**Privacy Rule Examples:**
- Users can only see their own data
- Public data visible to all
- Admin users see everything
- Paid users access premium content

#### 11:15-11:30 AM: Performance Considerations
**Instructor Activities:**
- Discuss search efficiency
- Show indexing concepts
- Explain data organization
- Set optimization mindset

---

### 11:30 AM - 12:30 PM: Design Your Database
**Duration:** 1 hour
**Type:** Self-directed with TA support

**Module 2.3: Data Modeling**

**Step 1: Core Data Types (20 min)**
Based on your MVP, create:
- [ ] User data type (if extending default)
- [ ] Main content type
- [ ] Supporting data types
- [ ] System configuration type

**Step 2: Field Definition (25 min)**
For each data type, define:
- Required fields
- Optional fields
- Default values
- Field constraints
- Relationships

**Step 3: Relationship Mapping (15 min)**
- [ ] Draw relationships on paper
- [ ] Identify foreign keys
- [ ] Check for circular references
- [ ] Plan list efficiency

**Common MVP Data Patterns:**
- **SaaS:** User → Account → Projects → Tasks
- **Marketplace:** User → Listings → Orders → Reviews
- **Social:** User → Posts → Comments → Likes
- **E-learning:** User → Courses → Lessons → Progress

---

### 12:30 PM - 1:30 PM: Lunch & Research
**Duration:** 1 hour
**Type:** Break + learning

**Research Activities:**
- Study similar apps' data structures
- Read Bubble database best practices
- Browse data schema examples
- Rest and recharge

---

### 1:30 PM - 2:30 PM: Implementation Sprint
**Duration:** 1 hour
**Type:** Hands-on building

**Build Your Database:**

**Phase 1: Create Data Types (20 min)**
1. Go to Data tab in Bubble
2. Create each data type
3. Add basic fields
4. Set up relationships

**Phase 2: Define Fields (25 min)**
1. Add all required fields
2. Set field types correctly
3. Configure privacy settings
4. Add field descriptions

**Phase 3: Test & Refine (15 min)**
1. Create sample data
2. Test relationships
3. Verify privacy rules
4. Adjust as needed

**Database Checklist:**
- [ ] All data types created
- [ ] Fields properly typed
- [ ] Relationships defined
- [ ] Privacy rules set
- [ ] Sample data added

---

### 2:30 PM - 3:00 PM: Office Hours - Database Q&A
**Duration:** 30 minutes
**Type:** Instructor-led

**Common Database Issues:**
- "Relationship not working"
- "Privacy rule blocking data"
- "Can't search efficiently"
- "Data structure seems wrong"

**Solutions & Patterns:**
- Debug privacy rules step-by-step
- Optimize search performance
- Restructure relationships
- Plan for scale early

---

### 3:00 PM - 4:00 PM: Privacy & Security Deep Dive
**Duration:** 1 hour
**Type:** Self-study + implementation

**Module 2.4: Security First**

**Privacy Rule Patterns (30 min):**

1. **User-Owned Data**
   ```
   When: Current user is Creator
   ```

2. **Public Content**
   ```
   When: Everyone (logged out)
   ```

3. **Role-Based Access**
   ```
   When: Current user's Role contains "Admin"
   ```

4. **Conditional Access**
   ```
   When: Current user is in This Item's Members
   ```

**Implementation Tasks (30 min):**
- [ ] Set up privacy rules for each data type
- [ ] Test with different user scenarios
- [ ] Verify admin access
- [ ] Check public data visibility
- [ ] Document access patterns

**Security Checklist:**
- [ ] No "Everyone" access to private data
- [ ] Users can't edit others' data
- [ ] Admin override rules work
- [ ] Public content clearly defined

---

### 4:00 PM - 5:00 PM: Performance Optimization
**Duration:** 1 hour
**Type:** Advanced concepts

**Search & Performance (30 min):**

**Efficient Search Patterns:**
- Index common search fields
- Limit data returned
- Use constraints wisely
- Avoid complex joins

**Data Organization:**
- Group related data
- Use consistent naming
- Plan for data growth
- Consider archived data

**Implementation (30 min):**
- [ ] Test search performance
- [ ] Optimize common queries
- [ ] Plan data archiving
- [ ] Set up monitoring

**Performance Tips:**
- Search on indexed fields
- Use "contains" sparingly
- Limit results with ":first item" or ":count"
- Cache expensive calculations

---

### 5:00 PM - 6:00 PM: Testing & Validation
**Duration:** 1 hour
**Type:** Quality assurance

**Database Testing Protocol:**

**Functional Testing (30 min):**
- [ ] Create sample users
- [ ] Add test data
- [ ] Test all relationships
- [ ] Verify privacy rules
- [ ] Check edge cases

**Scenarios to Test:**
- New user registration
- Data creation/editing
- Search functionality
- Privacy boundaries
- Admin functions

**Documentation (30 min):**
- [ ] Document data schema
- [ ] Record privacy decisions
- [ ] Note performance concerns
- [ ] Plan future enhancements

**End of Day Checklist:**
- [ ] Database fully designed
- [ ] Privacy rules implemented
- [ ] Testing completed
- [ ] Documentation updated
- [ ] Ready for UI building

---

## Common Database Mistakes

### Over-Normalization
**Problem:** Too many small tables
**Solution:** Balance normalization with usability

### Under-Securing
**Problem:** Too open privacy rules
**Solution:** Start restrictive, open as needed

### Poor Naming
**Problem:** Confusing field names
**Solution:** Clear, consistent naming conventions

### Missing Relationships
**Problem:** Data islands
**Solution:** Plan connections early

---

## Database Best Practices

### Naming Conventions:
- **Data Types:** PascalCase (User, BlogPost)
- **Fields:** lowercase_with_underscores
- **Relationships:** Clear descriptions

### Privacy Strategy:
- Default to private
- Explicit public data
- Test thoroughly
- Document decisions

### Performance Mindset:
- Think about search early
- Plan for growth
- Monitor usage
- Optimize iteratively

---

## Tomorrow's Preview

### Day 10: Component Building
- Reusable elements
- Custom components
- Style systems
- Responsive design

### Preparation:
- Review prototype design
- List repeating elements
- Plan component library
- Rest well for building day

---

## Resources

### Essential Reading:
- [Bubble Database Guide](#)
- [Privacy Rules Tutorial](#)
- [Performance Best Practices](#)
- [Data Schema Examples](#)

### Support Channels:
- #database-help in Discord
- Office hours for complex issues
- Peer review sessions
- TA async support

---

## Confidence Check

### Today's Achievements:
- Designed professional database
- Implemented security properly
- Planned for performance
- Ready for real building

### Tomorrow's Excitement:
- Building visual components
- Seeing design come alive
- Creating reusable elements
- Making progress visible

---

*"A solid foundation supports any height. Your database is the foundation—now we build up!"*