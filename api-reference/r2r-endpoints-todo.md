# R2R API Endpoints Documentation TODO

## Overview
This document tracks the progress of documenting all R2R API endpoints. The R2R API is organized into multiple router files, each handling different aspects of the system.

## Router Files Analysis

### ✅ Completed Analysis
- [x] `episodes_router.py` - 1 endpoint
- [x] `contradictions_router.py` - 1 endpoint  
- [x] `temporal_events_router.py` - 2 endpoints
- [x] `system_router.py` - 3 endpoints
- [x] `prompts_router.py` - 5 endpoints
- [x] `indices_router.py` - 4 endpoints
- [x] `chunks_router.py` - 5 endpoints
- [x] `conversations_router.py` - 8 endpoints
- [x] `retrieval_router.py` - 5 endpoints
- [x] `users_router.py` - 20+ endpoints
- [x] `collections_router.py` - 12 endpoints
- [x] `documents_router.py` - 15+ endpoints
- [x] `graph_router.py` - 20+ endpoints

### ✅ All Router Analysis Complete!

## Summary
- **Total Endpoints Identified**: ~100+ endpoints across 13 router files
- **Router Files Analyzed**: 13/13 (100% complete)
- **Documentation Status**: 15% complete (2/13 categories documented)
- **Completed Categories**: System, Documents
- **Remaining Categories**: 11 categories (Users, Collections, Chunks, Indices, Conversations, Retrieval, Prompts, Graph, Episodes, Contradictions, Temporal Events)

## Endpoint Categories

### 1. System & Health (3 endpoints)
- [ ] `GET /health` - Health check
- [ ] `GET /system/settings` - Get system settings (superuser only)
- [ ] `GET /system/status` - Get server status (superuser only)

### 2. Episodes (1 endpoint)
- [ ] `GET /episodes` - List episodes with filtering

### 3. Contradictions (1 endpoint)
- [ ] `POST /contradictions/{relationship_id}/cascade` - Cascade invalidation

### 4. Temporal Events (2 endpoints)
- [ ] `GET /temporal-events` - List temporal events with filtering
- [ ] `GET /temporal-events/{event_id}` - Get specific temporal event

### 5. Prompts (5 endpoints)
- [ ] `POST /prompts` - Create a new prompt
- [ ] `GET /prompts` - List all prompts
- [ ] `POST /prompts/{name}` - Get a specific prompt with inputs
- [ ] `PUT /prompts/{name}` - Update an existing prompt
- [ ] `DELETE /prompts/{name}` - Delete a prompt

### 6. Vector Indices (4 endpoints)
- [ ] `POST /indices` - Create vector index
- [ ] `GET /indices` - List vector indices
- [ ] `GET /indices/{table_name}/{index_name}` - Get vector index details
- [ ] `DELETE /indices/{table_name}/{index_name}` - Delete vector index

### 7. Chunks (5 endpoints)
- [ ] `POST /chunks/search` - Search chunks
- [ ] `GET /chunks/{id}` - Retrieve chunk
- [ ] `POST /chunks/{id}` - Update chunk
- [ ] `DELETE /chunks/{id}` - Delete chunk
- [ ] `GET /chunks` - List chunks

### 8. Conversations (8 endpoints)
- [ ] `POST /conversations` - Create conversation
- [ ] `GET /conversations` - List conversations
- [ ] `POST /conversations/export` - Export conversations to CSV
- [ ] `POST /conversations/export_messages` - Export messages to CSV
- [ ] `GET /conversations/{id}` - Get conversation details
- [ ] `POST /conversations/{id}` - Update conversation
- [ ] `DELETE /conversations/{id}` - Delete conversation
- [ ] `POST /conversations/{id}/messages` - Add message to conversation
- [ ] `POST /conversations/{id}/messages/{message_id}` - Update message in conversation

### 9. Retrieval (5 endpoints)
- [ ] `POST /retrieval/search` - Search R2R
- [ ] `POST /retrieval/rag` - RAG Query
- [ ] `POST /retrieval/agent` - RAG-powered Conversational Agent
- [ ] `POST /retrieval/completion` - Generate Message Completions
- [ ] `POST /retrieval/embedding` - Generate Embeddings

### 10. Users (20+ endpoints)
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
- [ ] `POST /users/{id}/api-keys` - Create user API key
- [ ] `GET /users/{id}/api-keys` - List user API keys
- [ ] `DELETE /users/{id}/api-keys/{key_id}` - Delete user API key
- [ ] `GET /users/{id}/limits` - Get user limits
- [ ] `GET /users/oauth/google/authorize` - Google OAuth authorization
- [ ] `GET /users/oauth/google/callback` - Google OAuth callback
- [ ] `GET /users/oauth/github/authorize` - GitHub OAuth authorization
- [ ] `GET /users/oauth/github/callback` - GitHub OAuth callback

### 11. Collections (12 endpoints)
- [ ] `POST /collections` - Create a new collection
- [ ] `POST /collections/export` - Export collections to CSV
- [ ] `GET /collections` - List collections
- [ ] `GET /collections/{id}` - Get collection details
- [ ] `POST /collections/{id}` - Update collection
- [ ] `DELETE /collections/{id}` - Delete collection
- [ ] `POST /collections/{id}/documents/{document_id}` - Add document to collection
- [ ] `GET /collections/{id}/documents` - List documents in collection
- [ ] `DELETE /collections/{id}/documents/{document_id}` - Remove document from collection
- [ ] `GET /collections/{id}/users` - List users in collection
- [ ] `POST /collections/{id}/users/{user_id}` - Add user to collection
- [ ] `DELETE /collections/{id}/users/{user_id}` - Remove user from collection
- [ ] `POST /collections/{id}/extract` - Extract entities and relationships
- [ ] `GET /collections/name/{collection_name}` - Get a collection by name

### 12. Documents (15+ endpoints)
- [ ] `POST /documents` - Create a new document
- [ ] `PATCH /documents/{id}/metadata` - Append metadata to a document
- [ ] `PUT /documents/{id}/metadata` - Replace metadata of a document
- [ ] `POST /documents/export` - Export documents to CSV
- [ ] `GET /documents/download_zip` - Export multiple documents as zip
- [ ] `GET /documents` - List documents
- [ ] `GET /documents/{id}` - Retrieve a document
- [ ] `GET /documents/{id}/chunks` - List document chunks
- [ ] `GET /documents/{id}/file` - Download document file
- [ ] `DELETE /documents/by-filter` - Delete documents by filter
- [ ] `DELETE /documents/{id}` - Delete a document
- [ ] `GET /documents/{id}/collections` - List document collections
- [ ] `POST /documents/{id}/extract` - Extract entities and relationships
- [ ] `POST /documents/{id}/deduplicate` - Deduplicate entities
- [ ] `GET /documents/{id}/entities` - Lists the entities from the document
- [ ] `POST /documents/{id}/entities/export` - Export document entities to CSV
- [ ] `GET /documents/{id}/relationships` - List document relationships
- [ ] `POST /documents/{id}/relationships/export` - Export document relationships to CSV

### 13. Graph (20+ endpoints)
- [ ] `GET /graphs` - List graphs
- [ ] `GET /graphs/{collection_id}` - Retrieve graph details
- [ ] `POST /graphs/{collection_id}/communities/build` - Build communities
- [ ] `POST /graphs/{collection_id}/reset` - Reset a graph back to the initial state
- [ ] `POST /graphs/{collection_id}` - Update graph
- [ ] `GET /graphs/{collection_id}/entities` - List graph entities
- [ ] `POST /graphs/{collection_id}/entities/export` - Export graph entities to CSV
- [ ] `POST /graphs/{collection_id}/entities` - Create a new entity
- [ ] `POST /graphs/{collection_id}/relationships` - Create a new relationship
- [ ] `POST /graphs/{collection_id}/relationships/export` - Export graph relationships to CSV
- [ ] `GET /graphs/{collection_id}/entities/{entity_id}` - Retrieve a specific entity
- [ ] `POST /graphs/{collection_id}/entities/{entity_id}` - Update an entity
- [ ] `DELETE /graphs/{collection_id}/entities/{entity_id}` - Delete an entity
- [ ] `GET /graphs/{collection_id}/relationships/{relationship_id}` - Retrieve a specific relationship
- [ ] `POST /graphs/{collection_id}/relationships/{relationship_id}` - Update a relationship
- [ ] `DELETE /graphs/{collection_id}/relationships/{relationship_id}` - Delete a relationship
- [ ] `POST /graphs/{collection_id}/communities` - Create a new community
- [ ] `GET /graphs/{collection_id}/communities` - List communities
- [ ] `GET /graphs/{collection_id}/communities/{community_id}` - Retrieve a community
- [ ] `DELETE /graphs/{collection_id}/communities/{community_id}` - Delete a community
- [ ] `POST /graphs/{collection_id}/communities/export` - Export communities to CSV
- [ ] `POST /graphs/{collection_id}/communities/{community_id}` - Update community
- [ ] `POST /graphs/{collection_id}/pull` - Pull latest entities to the graph

## Documentation Tasks

### Phase 1: Complete Analysis (Current)
- [ ] Analyze remaining large router files
- [ ] Create complete endpoint inventory
- [ ] Categorize endpoints by functionality

### Phase 2: Documentation Creation
- [ ] Create individual endpoint documentation files
- [ ] Add code examples for each endpoint
- [ ] Include request/response schemas
- [ ] Add authentication requirements
- [ ] Document rate limiting

### Phase 3: Organization
- [ ] Create index pages for each category
- [ ] Add navigation between related endpoints
- [ ] Create overview pages for each router
- [ ] Add cross-references between related endpoints

### Phase 4: Quality Assurance
- [ ] Review all documentation for accuracy
- [ ] Test code examples
- [ ] Verify authentication requirements
- [ ] Check for consistency in formatting

## Notes
- Total estimated endpoints: 50+ (based on file sizes and complexity)
- Large router files contain multiple endpoints with complex functionality
- Some endpoints have rate limiting and authentication requirements
- Many endpoints include code examples in multiple languages (Python, JavaScript, cURL)
- Documentation should follow existing Mintlify format in docs/api-reference/ 