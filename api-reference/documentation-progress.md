# R2R API Documentation Progress

## Overview

This document tracks the progress of creating comprehensive API documentation for all R2R endpoints. The goal is to document every single endpoint in the R2R API v3.

## Current Status

**Overall Progress**: 15% Complete (2/13 categories)
**Mintlify Configuration**: ✅ Updated to use new R2R API structure

### ✅ Completed Categories

#### 1. System Operations (3 endpoints)
- ✅ `GET /health` - Health check
- ✅ `GET /config` - Get configuration  
- ✅ `GET /status` - Get system status
- **Documentation**: [system.mdx](./system.mdx)

#### 2. Document Management (19 endpoints)
- ✅ `POST /documents` - Create document
- ✅ `GET /documents` - List documents
- ✅ `GET /documents/{id}` - Get document
- ✅ `PATCH /documents/{id}/metadata` - Update metadata
- ✅ `PUT /documents/{id}/metadata` - Replace metadata
- ✅ `GET /documents/{id}/chunks` - Get document chunks
- ✅ `GET /documents/{id}/file` - Download document file
- ✅ `POST /documents/export` - Export documents
- ✅ `GET /documents/download_zip` - Download multiple documents
- ✅ `DELETE /documents/{id}` - Delete document
- ✅ `DELETE /documents/by-filter` - Delete documents by filter
- ✅ `GET /documents/{id}/collections` - Get document collections
- ✅ `POST /documents/{id}/extract` - Extract entities
- ✅ `POST /documents/{id}/deduplicate` - Deduplicate entities
- ✅ `GET /documents/{id}/entities` - Get document entities
- ✅ `POST /documents/{id}/entities/export` - Export entities
- ✅ `GET /documents/{id}/relationships` - Get relationships
- ✅ `POST /documents/{id}/relationships/export` - Export relationships
- **Documentation**: [documents.mdx](./documents.mdx)

### 🔄 In Progress Categories

None currently in progress.

### ⏳ Pending Categories

#### 3. User Management (20+ endpoints)
- [ ] `POST /users` - Create user (register)
- [ ] `POST /users/export` - Export users to CSV
- [ ] `POST /users/verify-email` - Verify email address
- [ ] `POST /users/send-verification-email` - Send verification email
- [ ] `POST /users/login` - User login
- [ ] `POST /users/logout` - User logout
- [ ] `POST /users/refresh-token` - Refresh access token
- [ ] `POST /users/change-password` - Change password
- [ ] `POST /users/request-password-reset` - Request password reset
- [ ] `POST /users/reset-password` - Reset password
- [ ] `GET /users` - List users
- [ ] `GET /users/{id}` - Get user details
- [ ] `POST /users/{id}` - Update user
- [ ] `DELETE /users/{id}` - Delete user
- [ ] `GET /users/{id}/collections` - Get user collections
- [ ] `POST /users/{id}/collections/{collection_id}` - Add user to collection
- [ ] `DELETE /users/{id}/collections/{collection_id}` - Remove user from collection
- [ ] `GET /users/{id}/documents` - Get user documents
- [ ] `GET /users/{id}/conversations` - Get user conversations
- [ ] `GET /users/{id}/api-keys` - Get user API keys
- [ ] `POST /users/{id}/api-keys` - Create API key
- [ ] `DELETE /users/{id}/api-keys/{key_id}` - Delete API key
- **Priority**: High (Core functionality)
- **Estimated Time**: 4-6 hours

#### 4. Collection Management (12 endpoints)
- [ ] `POST /collections` - Create collection
- [ ] `POST /collections/export` - Export collections
- [ ] `GET /collections` - List collections
- [ ] `GET /collections/{id}` - Get collection
- [ ] `POST /collections/{id}` - Update collection
- [ ] `DELETE /collections/{id}` - Delete collection
- [ ] `POST /collections/{id}/documents/{document_id}` - Add document to collection
- [ ] `GET /collections/{id}/documents` - List documents in collection
- [ ] `DELETE /collections/{id}/documents/{document_id}` - Remove document from collection
- [ ] `GET /collections/{id}/users` - List users in collection
- [ ] `POST /collections/{id}/users/{user_id}` - Add user to collection
- [ ] `DELETE /collections/{id}/users/{user_id}` - Remove user from collection
- [ ] `GET /collections/name/{collection_name}` - Get collection by name
- **Priority**: High (Core functionality)
- **Estimated Time**: 3-4 hours

#### 5. Retrieval Operations (5 endpoints)
- [ ] `POST /retrieval/search` - Search R2R
- [ ] `POST /retrieval/rag` - RAG Query
- [ ] `POST /retrieval/agent` - RAG-powered Conversational Agent
- [ ] `POST /retrieval/completion` - Generate Message Completions
- [ ] `POST /retrieval/embedding` - Generate Embeddings
- **Priority**: High (Core functionality)
- **Estimated Time**: 2-3 hours

#### 6. Conversations (8 endpoints)
- [ ] `POST /conversations` - Create conversation
- [ ] `GET /conversations` - List conversations
- [ ] `GET /conversations/{id}` - Get conversation
- [ ] `POST /conversations/{id}` - Update conversation
- [ ] `DELETE /conversations/{id}` - Delete conversation
- [ ] `POST /conversations/{id}/messages` - Add message to conversation
- [ ] `GET /conversations/{id}/messages` - List conversation messages
- [ ] `DELETE /conversations/{id}/messages/{message_id}` - Delete message
- **Priority**: Medium
- **Estimated Time**: 2-3 hours

#### 7. Knowledge Graph (20+ endpoints)
- [ ] `GET /graphs` - List graphs
- [ ] `GET /graphs/{collection_id}` - Get graph details
- [ ] `POST /graphs/{collection_id}/communities/build` - Build communities
- [ ] `POST /graphs/{collection_id}/reset` - Reset graph
- [ ] `POST /graphs/{collection_id}` - Update graph
- [ ] `GET /graphs/{collection_id}/entities` - List graph entities
- [ ] `POST /graphs/{collection_id}/entities/export` - Export entities
- [ ] `POST /graphs/{collection_id}/entities` - Create entity
- [ ] `POST /graphs/{collection_id}/relationships` - Create relationship
- [ ] `POST /graphs/{collection_id}/relationships/export` - Export relationships
- [ ] `GET /graphs/{collection_id}/entities/{entity_id}` - Get entity
- [ ] `POST /graphs/{collection_id}/entities/{entity_id}` - Update entity
- [ ] `DELETE /graphs/{collection_id}/entities/{entity_id}` - Delete entity
- [ ] `GET /graphs/{collection_id}/relationships/{relationship_id}` - Get relationship
- [ ] `POST /graphs/{collection_id}/relationships/{relationship_id}` - Update relationship
- [ ] `DELETE /graphs/{collection_id}/relationships/{relationship_id}` - Delete relationship
- [ ] `POST /graphs/{collection_id}/communities` - Create community
- [ ] `GET /graphs/{collection_id}/communities` - List communities
- [ ] `GET /graphs/{collection_id}/communities/{community_id}` - Get community
- [ ] `DELETE /graphs/{collection_id}/communities/{community_id}` - Delete community
- [ ] `POST /graphs/{collection_id}/communities/export` - Export communities
- [ ] `POST /graphs/{collection_id}/communities/{community_id}` - Update community
- [ ] `POST /graphs/{collection_id}/pull` - Pull latest entities
- **Priority**: Medium
- **Estimated Time**: 4-5 hours

#### 8. Chunk Management (5 endpoints)
- [ ] `GET /chunks` - List chunks
- [ ] `GET /chunks/{id}` - Get chunk
- [ ] `POST /chunks/{id}` - Update chunk
- [ ] `DELETE /chunks/{id}` - Delete chunk
- [ ] `POST /chunks/search` - Search chunks
- **Priority**: Low
- **Estimated Time**: 1-2 hours

#### 9. Index Management (4 endpoints)
- [ ] `POST /indices` - Create index
- [ ] `GET /indices` - List indices
- [ ] `GET /indices/{id}` - Get index
- [ ] `DELETE /indices/{id}` - Delete index
- **Priority**: Low
- **Estimated Time**: 1-2 hours

#### 10. Prompt Management (5 endpoints)
- [ ] `POST /prompts` - Create prompt
- [ ] `GET /prompts` - List prompts
- [ ] `GET /prompts/{id}` - Get prompt
- [ ] `POST /prompts/{id}` - Update prompt
- [ ] `DELETE /prompts/{id}` - Delete prompt
- **Priority**: Low
- **Estimated Time**: 1-2 hours

#### 11. Episodes (1 endpoint)
- [ ] `GET /episodes` - List episodes
- **Priority**: Low
- **Estimated Time**: 30 minutes

#### 12. Contradictions (1 endpoint)
- [ ] `GET /contradictions` - List contradictions
- **Priority**: Low
- **Estimated Time**: 30 minutes

#### 13. Temporal Events (2 endpoints)
- [ ] `GET /temporal-events` - List temporal events
- [ ] `POST /temporal-events` - Create temporal event
- **Priority**: Low
- **Estimated Time**: 1 hour

## Next Steps

### ✅ Completed
- **Mintlify Configuration Updated** - Navigation now points to new R2R API structure
- **Placeholder Files Created** - All API categories have placeholder pages
- **Old Documentation Removed** - Cleaned up old placeholder files

### Immediate Priority (Next 1-2 days)
1. **User Management** - Complete user authentication and management endpoints
2. **Collection Management** - Document collection CRUD operations
3. **Retrieval Operations** - Document core search and RAG functionality

### Medium Priority (Next 3-5 days)
4. **Conversations** - Document chat and conversation management
5. **Knowledge Graph** - Document graph operations and entity management

### Low Priority (Next week)
6. **Chunk Management** - Document text chunk operations
7. **Index Management** - Document search index operations
8. **Prompt Management** - Document prompt template operations
9. **Remaining endpoints** - Episodes, Contradictions, Temporal Events

## Documentation Standards

Each endpoint documentation should include:

1. **Endpoint information**: Method, path, description
2. **Authentication requirements**
3. **Request parameters** (path, query, body)
4. **Response format** with example
5. **Error codes** and descriptions
6. **Rate limiting information**
7. **SDK examples** (Python and JavaScript)
8. **cURL examples**

## File Structure

```
docs/api-reference/
├── r2r-api-reference.mdx          # Main API reference index
├── system.mdx                     # ✅ System operations
├── documents.mdx                  # ✅ Document management
├── users.mdx                      # ⏳ User management
├── collections.mdx                # ⏳ Collection management
├── retrieval.mdx                  # ⏳ Retrieval operations
├── conversations.mdx              # ⏳ Conversation management
├── graph.mdx                      # ⏳ Knowledge graph
├── chunks.mdx                     # ⏳ Chunk management
├── indices.mdx                    # ⏳ Index management
├── prompts.mdx                    # ⏳ Prompt management
├── episodes.mdx                   # ⏳ Episode management
├── contradictions.mdx             # ⏳ Contradiction detection
├── temporal-events.mdx            # ⏳ Temporal events
├── r2r-endpoints-todo.md          # Detailed TODO list
└── documentation-progress.md      # This progress file
```

## Time Estimates

- **Total estimated time**: 20-25 hours
- **Completed**: 3-4 hours (15%)
- **Remaining**: 17-21 hours (85%)
- **Estimated completion**: 1-2 weeks with focused effort

## Quality Assurance

Before marking any category as complete:

1. ✅ All endpoints documented with full details
2. ✅ Request/response examples provided
3. ✅ Error codes documented
4. ✅ SDK examples included
5. ✅ cURL examples provided
6. ✅ Rate limiting information included
7. ✅ Cross-references to related endpoints
8. ✅ Consistent formatting and structure 