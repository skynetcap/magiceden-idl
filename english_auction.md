```json
version: "3.1.0",
name: "english_auction",
instructions: [{
    name: "createAuction",
    accounts: [{
        name: "payer",
        isMut: !0,
        isSigner: !0
    }, {
        name: "sourceTokenAccount",
        isMut: !0,
        isSigner: !1
    }, {
        name: "tokenAccount",
        isMut: !0,
        isSigner: !1
    }, {
        name: "tokenMint",
        isMut: !1,
        isSigner: !1
    }, {
        name: "config",
        isMut: !0,
        isSigner: !0
    }, {
        name: "programAsSigner",
        isMut: !1,
        isSigner: !1
    }, {
        name: "metadata",
        isMut: !1,
        isSigner: !1
    }, {
        name: "edition",
        isMut: !1,
        isSigner: !1
    }, {
        name: "systemProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "tokenProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "associatedTokenProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "rent",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "args",
        type: {
            defined: "CreateAuctionArgs"
        }
    }]
}, {
    name: "updateAuction",
    accounts: [{
        name: "authority",
        isMut: !0,
        isSigner: !0
    }, {
        name: "config",
        isMut: !0,
        isSigner: !1
    }, {
        name: "systemProgram",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "args",
        type: {
            defined: "UpdateAuctionArgs"
        }
    }]
}, {
    name: "placeBidV2",
    accounts: [{
        name: "payer",
        isMut: !0,
        isSigner: !0
    }, {
        name: "authority",
        isMut: !1,
        isSigner: !1
    }, {
        name: "config",
        isMut: !0,
        isSigner: !1
    }, {
        name: "bid",
        isMut: !0,
        isSigner: !1
    }, {
        name: "bidEscrow",
        isMut: !0,
        isSigner: !1
    }, {
        name: "systemProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "rent",
        isMut: !1,
        isSigner: !1
    }, {
        name: "clock",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "bidBump",
        type: "u8"
    }, {
        name: "escrowBump",
        type: "u8"
    }, {
        name: "amount",
        type: "u64"
    }]
}, {
    name: "cancelAuction",
    accounts: [{
        name: "authority",
        isMut: !0,
        isSigner: !0
    }, {
        name: "config",
        isMut: !0,
        isSigner: !1
    }, {
        name: "tokenAccount",
        isMut: !0,
        isSigner: !1
    }, {
        name: "tokenMint",
        isMut: !1,
        isSigner: !1
    }, {
        name: "destinationTokenAccount",
        isMut: !0,
        isSigner: !1
    }, {
        name: "programAsSigner",
        isMut: !1,
        isSigner: !1
    }, {
        name: "systemProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "tokenProgram",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "programAsSignerBump",
        type: "u8"
    }]
}, {
    name: "settleV2",
    accounts: [{
        name: "payer",
        isMut: !0,
        isSigner: !0
    }, {
        name: "authority",
        isMut: !0,
        isSigner: !1
    }, {
        name: "tokenAccount",
        isMut: !0,
        isSigner: !1
    }, {
        name: "tokenMint",
        isMut: !1,
        isSigner: !1
    }, {
        name: "config",
        isMut: !0,
        isSigner: !1
    }, {
        name: "winningBid",
        isMut: !0,
        isSigner: !1
    }, {
        name: "winningBidder",
        isMut: !1,
        isSigner: !1
    }, {
        name: "winnerAta",
        isMut: !0,
        isSigner: !1
    }, {
        name: "alternateTokenAccount",
        isMut: !0,
        isSigner: !0
    }, {
        name: "winnerEscrow",
        isMut: !0,
        isSigner: !1
    }, {
        name: "programAsSigner",
        isMut: !1,
        isSigner: !1
    }, {
        name: "metadata",
        isMut: !1,
        isSigner: !1
    }, {
        name: "feeAccount",
        isMut: !0,
        isSigner: !1
    }, {
        name: "systemProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "tokenProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "associatedTokenProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "clock",
        isMut: !1,
        isSigner: !1
    }, {
        name: "rent",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "programAsSignerBump",
        type: "u8"
    }]
}],
accounts: [{
    name: "auctionConfigV2",
    type: {
        kind: "struct",
        fields: [{
            name: "bump",
            type: "u8"
        }, {
            name: "authority",
            type: "publicKey"
        }, {
            name: "minBid",
            type: "u64"
        }, {
            name: "minBidIncrement",
            type: "u64"
        }, {
            name: "startDate",
            type: "i64"
        }, {
            name: "endDate",
            type: "i64"
        }, {
            name: "tokenAccount",
            type: "publicKey"
        }, {
            name: "tokenMint",
            type: "publicKey"
        }, {
            name: "highestBid",
            type: {
                option: "publicKey"
            }
        }, {
            name: "highestBidAmount",
            type: {
                option: "u64"
            }
        }, {
            name: "highestBidder",
            type: {
                option: "publicKey"
            }
        }, {
            name: "acceptingBids",
            type: "bool"
        }, {
            name: "auctionClosed",
            type: "bool"
        }, {
            name: "timeExtension",
            type: "i64"
        }, {
            name: "timeExtensionThreshold",
            type: "i64"
        }, {
            name: "payees",
            type: {
                vec: {
                    defined: "Payee"
                }
            }
        }]
    }
}, {
    name: "bid",
    type: {
        kind: "struct",
        fields: [{
            name: "bump",
            type: "u8"
        }, {
            name: "escrowBump",
            type: "u8"
        }, {
            name: "bidder",
            type: "publicKey"
        }, {
            name: "amount",
            type: "u64"
        }, {
            name: "auctionConfig",
            type: "publicKey"
        }, {
            name: "timestamp",
            type: "i64"
        }]
    }
}],
types: [{
    name: "CreateAuctionArgs",
    type: {
        kind: "struct",
        fields: [{
            name: "programAsSignerBump",
            type: "u8"
        }, {
            name: "minBid",
            type: "u64"
        }, {
            name: "minBidIncrement",
            type: "u64"
        }, {
            name: "startDate",
            type: "i64"
        }, {
            name: "endDate",
            type: "i64"
        }, {
            name: "timeExtension",
            type: "i64"
        }, {
            name: "timeExtensionThreshold",
            type: "i64"
        }, {
            name: "payees",
            type: {
                vec: {
                    defined: "Payee"
                }
            }
        }]
    }
}, {
    name: "UpdateAuctionArgs",
    type: {
        kind: "struct",
        fields: [{
            name: "startDate",
            type: {
                option: "i64"
            }
        }, {
            name: "endDate",
            type: {
                option: "i64"
            }
        }, {
            name: "minBid",
            type: {
                option: "u64"
            }
        }, {
            name: "minBidIncrement",
            type: {
                option: "u64"
            }
        }, {
            name: "acceptingBids",
            type: {
                option: "bool"
            }
        }, {
            name: "timeExtension",
            type: {
                option: "i64"
            }
        }, {
            name: "timeExtensionThreshold",
            type: {
                option: "i64"
            }
        }, {
            name: "payees",
            type: {
                option: {
                    vec: {
                        defined: "Payee"
                    }
                }
            }
        }]
    }
}, {
    name: "Payee",
    type: {
        kind: "struct",
        fields: [{
            name: "address",
            type: "publicKey"
        }, {
            name: "share",
            type: "u8"
        }]
    }
}],
errors: [{
    code: 6e3,
    name: "NumericalOverflow",
    msg: "Numerical overflow"
}, {
    code: 6001,
    name: "DerivedKeyInvalid",
    msg: "Derived key invalid"
}, {
    code: 6002,
    name: "AuctionNotAcceptingBids",
    msg: "Auction is currently not accepting bids"
}, {
    code: 6003,
    name: "AuctionNotStarted",
    msg: "Auction has not started"
}, {
    code: 6004,
    name: "AuctionEnded",
    msg: "Auction has ended"
}, {
    code: 6005,
    name: "BidBelowMinBid",
    msg: "Bid is below minimum bid"
}, {
    code: 6006,
    name: "NewBidTooSmall",
    msg: "New bid must be greater than previous bid"
}, {
    code: 6007,
    name: "BidIncrementTooSmall",
    msg: "Bid must exceed current max bid by at least bid_increment"
}, {
    code: 6008,
    name: "CannotSettleAuctionNotEnded",
    msg: "Cannot settle auction since auction has not ended"
}, {
    code: 6009,
    name: "ReservePriceNotMet",
    msg: "Cannot settle auction since reserve price not met"
}, {
    code: 6010,
    name: "AuctionTokenDelegateInvalid",
    msg: "Auction token delegate must be program"
}, {
    code: 6011,
    name: "InvalidPrevBid",
    msg: "Invalid prev_bid does not match auction current highest bid"
}, {
    code: 6012,
    name: "InvalidPrevBidder",
    msg: "Invalid highest_bidder does not match auction current highest bidder"
}, {
    code: 6013,
    name: "CannotSettleClosedAuction",
    msg: "Cannot settle after auction is closed"
}, {
    code: 6014,
    name: "CannotWithdrawTopBidEscrow",
    msg: "Cannot withdraw from escrow of top bid"
}, {
    code: 6015,
    name: "CannotUpdateClosedAuction",
    msg: "Cannot update a closed auction"
}, {
    code: 6016,
    name: "CannotCloseAuctionBeforeEndDate",
    msg: "Cannot close auction before end date"
}, {
    code: 6017,
    name: "CannotWithdrawEscrowBeforeEndDate",
    msg: "Cannot withdraw from escrow before end date"
}, {
    code: 6018,
    name: "AuctionTokenAccountBalanceInvalid",
    msg: "Auction token account must have at least 1 token"
}, {
    code: 6019,
    name: "AuctionTokenAccountOwnerInvalid",
    msg: "Auction token account must be owned by program_as_signer"
}, {
    code: 6020,
    name: "AuctionTimeExtensionNegative",
    msg: "Auction time_extension cannot be negative"
}, {
    code: 6021,
    name: "AuctionTimeExtensionThresholdNegative",
    msg: "Auction time_extension_threshold cannot be negative"
}, {
    code: 6022,
    name: "CannotUpdateAuctionAfterStart",
    msg: "Cannot update auction after auction has started"
}, {
    code: 6023,
    name: "CannotBidClosedAuction",
    msg: "Cannot bid on closed auction"
}, {
    code: 6024,
    name: "PayeeSharesInvalidSum",
    msg: "Payee shares must sum to 100"
}, {
    code: 6025,
    name: "InvalidNumPayees",
    msg: "Payee count must be between 1 and 5"
}, {
    code: 6026,
    name: "PayeeSharesZero",
    msg: "Payee cannot have 0 shares"
}, {
    code: 6027,
    name: "MismatchedPayees",
    msg: "Payee address given do not match those in config"
}, {
    code: 6028,
    name: "AlternateTokenAccountAlreadyInUse",
    msg: "Alternate token account is already in use"
}, {
    code: 6029,
    name: "KeysNotEqual",
    msg: "Keys not equal"
}, {
    code: 6030,
    name: "InvalidBump",
    msg: "Bump invalid"
}, {
    code: 6031,
    name: "AccountNotInitialized",
    msg: "Account not initialized"
}, {
    code: 6032,
    name: "InvalidNumCreators",
    msg: "Invalid number of creators in settle"
}, {
    code: 6033,
    name: "InvalidAuctionAuthority",
    msg: "Invalid auction authority"
}, {
    code: 6034,
    name: "CannotCancelAuctionAfterBid",
    msg: "Cannot cancel auction after bid has been placed"
}, {
    code: 6035,
    name: "CannotCancelActiveAuction",
    msg: "Cannot cancel auction while it is active"
}, {
    code: 6036,
    name: "InvalidMint",
    msg: "Invalid mint"
}, {
    code: 6037,
    name: "InvalidTokenAccountOwner",
    msg: "Invalid token account owner"
}, {
    code: 6038,
    name: "InvalidEdition",
    msg: "Edition Key invalid"
}, {
    code: 6039,
    name: "EndDateBeforeStartDate",
    msg: "End date must be after start date"
}]
}
```