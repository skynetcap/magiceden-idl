```json
version: "0.1.0",
name: "dutch_auction",
instructions: [{
    name: "createDutchAuction",
    accounts: [{
        name: "payer",
        isMut: !0,
        isSigner: !0
    }, {
        name: "tokenAccount",
        isMut: !1,
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
        name: "programAsSigner",
        isMut: !1,
        isSigner: !1
    }, {
        name: "systemProgram",
        isMut: !1,
        isSigner: !1
    }, {
        name: "rent",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "configBump",
        type: "u8"
    }, {
        name: "programAsSignerBump",
        type: "u8"
    }, {
        name: "minPriceLevel",
        type: "u64"
    }, {
        name: "maxPriceLevel",
        type: "u64"
    }, {
        name: "maxBidAmount",
        type: "u32"
    }, {
        name: "priceIncrement",
        type: "u64"
    }, {
        name: "auctionAmount",
        type: "u32"
    }, {
        name: "startDate",
        type: "i64"
    }, {
        name: "endDate",
        type: "i64"
    }]
}, {
    name: "updateDutchAuction",
    accounts: [{
        name: "authority",
        isMut: !0,
        isSigner: !0
    }, {
        name: "config",
        isMut: !0,
        isSigner: !1
    }, {
        name: "clock",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "maxBidAmount",
        type: {
            option: "u32"
        }
    }, {
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
        name: "acceptingBids",
        type: {
            option: "bool"
        }
    }]
}, {
    name: "placeBid",
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
        name: "sequenceTracker",
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
        name: "sequenceTrackerBump",
        type: "u8"
    }, {
        name: "sequenceNumber",
        type: "u8"
    }, {
        name: "bidPrice",
        type: "u64"
    }, {
        name: "bidAmount",
        type: "u32"
    }]
}, {
    name: "updateBid",
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
        name: "clock",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "sequenceNumber",
        type: "u8"
    }, {
        name: "bidPrice",
        type: {
            option: "u64"
        }
    }, {
        name: "bidAmount",
        type: {
            option: "u32"
        }
    }]
}, {
    name: "settleBid",
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
        name: "bid",
        isMut: !0,
        isSigner: !1
    }, {
        name: "bidder",
        isMut: !0,
        isSigner: !1
    }, {
        name: "bidderAta",
        isMut: !0,
        isSigner: !1
    }, {
        name: "bidEscrow",
        isMut: !0,
        isSigner: !1
    }, {
        name: "sequenceTracker",
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
    }, {
        name: "sequenceNumber",
        type: "u8"
    }]
}, {
    name: "mintAfterEnd",
    accounts: [{
        name: "payer",
        isMut: !0,
        isSigner: !0
    }, {
        name: "authority",
        isMut: !0,
        isSigner: !1
    }, {
        name: "payerAta",
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
    }, {
        name: "amount",
        type: "u32"
    }]
}, {
    name: "cancelBid",
    accounts: [{
        name: "payer",
        isMut: !1,
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
        name: "bidder",
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
        name: "sequenceTracker",
        isMut: !0,
        isSigner: !1
    }, {
        name: "clock",
        isMut: !1,
        isSigner: !1
    }, {
        name: "systemProgram",
        isMut: !1,
        isSigner: !1
    }],
    args: [{
        name: "sequenceNumber",
        type: "u8"
    }]
}],
accounts: [{
    name: "dutchAuctionConfig",
    type: {
        kind: "struct",
        fields: [{
            name: "bump",
            type: "u8"
        }, {
            name: "authority",
            type: "publicKey"
        }, {
            name: "minPriceLevel",
            type: "u64"
        }, {
            name: "maxPriceLevel",
            type: "u64"
        }, {
            name: "maxBidAmount",
            type: "u32"
        }, {
            name: "priceIncrement",
            type: "u64"
        }, {
            name: "auctionAmount",
            type: "u32"
        }, {
            name: "amountSettlable",
            type: "u32"
        }, {
            name: "amountSettled",
            type: "u32"
        }, {
            name: "startDate",
            type: "i64"
        }, {
            name: "endDate",
            type: "i64"
        }, {
            name: "settlePrice",
            type: "u64"
        }, {
            name: "tokenAccount",
            type: "publicKey"
        }, {
            name: "tokenMint",
            type: "publicKey"
        }, {
            name: "acceptingBids",
            type: "bool"
        }, {
            name: "bidAmountPerPriceLevel",
            type: {
                vec: "u32"
            }
        }, {
            name: "settleAmountPerPriceLevel",
            type: {
                vec: "u32"
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
            name: "sequenceTrackerBump",
            type: "u8"
        }, {
            name: "bidder",
            type: "publicKey"
        }, {
            name: "bidPrice",
            type: "u64"
        }, {
            name: "bidAmount",
            type: "u32"
        }, {
            name: "auctionConfig",
            type: "publicKey"
        }]
    }
}, {
    name: "sequenceTracker",
    type: {
        kind: "struct",
        fields: [{
            name: "bump",
            type: "u8"
        }, {
            name: "currentSequence",
            type: "u8"
        }, {
            name: "bidsSettled",
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
    name: "AuctionAmountZero",
    msg: "Auction cannot have 0 auction amount"
}, {
    code: 6003,
    name: "AuctionTokenAccountBalanceInvalid",
    msg: "Auction token account must have the exact number of tokens planned to be auctioned off"
}, {
    code: 6004,
    name: "AuctionTokenAccountOwnerInvalid",
    msg: "Auction token account must be owned by program_as_signer"
}, {
    code: 6005,
    name: "FlippedPriceLevels",
    msg: "Auction max price level must be greater than or equal to min price level"
}, {
    code: 6006,
    name: "InvalidIntervals",
    msg: "Difference between max and min price must be divisible by price interval"
}, {
    code: 6007,
    name: "InvalidTime",
    msg: "Given start and end times are invalid"
}, {
    code: 6008,
    name: "UpdateAuctionAfterEnd",
    msg: "Cannot update an auction after it has passed the ending time"
}, {
    code: 6009,
    name: "UpdateAuctionStartAfterStart",
    msg: "Cannot update auction start time after it has already started"
}, {
    code: 6010,
    name: "AuctionNotAcceptingBids",
    msg: "Auction is currently not accepting bids"
}, {
    code: 6011,
    name: "AuctionNotStarted",
    msg: "Auction has not started yet"
}, {
    code: 6012,
    name: "AuctionEnded",
    msg: "Auction has already ended"
}, {
    code: 6013,
    name: "BidZeroAmount",
    msg: "Cannot bid for a zero amount"
}, {
    code: 6014,
    name: "BidPriceTooLow",
    msg: "Bid price is below the minimum accepted price"
}, {
    code: 6015,
    name: "BidPriceTooHigh",
    msg: "Bid price is above the maximum accepted price"
}, {
    code: 6016,
    name: "BidPriceNotInInterval",
    msg: "Bid price does not fall evenly into a price interval"
}, {
    code: 6017,
    name: "UnsupportedSequenceNumber",
    msg: "New sequence number will not be supported"
}, {
    code: 6018,
    name: "SequenceNumberMismatch",
    msg: "Given sequence number does not match expected sequence number"
}, {
    code: 6019,
    name: "UpdateBidLowerPrice",
    msg: "Cannot update bid to a lower price"
}, {
    code: 6020,
    name: "UpdateBidLowerAmount",
    msg: "Cannot update bid to a lower amount"
}, {
    code: 6021,
    name: "CannotSettleAuctionNotEnded",
    msg: "Cannot settle a bid when an auction has not ended"
}, {
    code: 6022,
    name: "AuctionTokenDelegateInvalid",
    msg: "Auction token delegate must be program"
}, {
    code: 6023,
    name: "MintAuctionNotEnded",
    msg: "Auction cannot mint at min price before it ends"
}, {
    code: 6024,
    name: "MintZeroAmount",
    msg: "Auction cannot mint zero tokens at min price"
}, {
    code: 6025,
    name: "MintAuctionNotSettled",
    msg: "Auction cannot mint at min price since all winning bids have not been settled"
}, {
    code: 6026,
    name: "MultipleBids",
    msg: "Auction currently only supports one bid with sequence number 1"
}, {
    code: 6027,
    name: "CancelEnded",
    msg: "Cannot cancel a bid after auction has ended. Please use the settle bid instruction"
}, {
    code: 6028,
    name: "CancelAboveSettlement",
    msg: "Cannot cancel a bid that is above the current settlement price"
}, {
    code: 6029,
    name: "MaxBidAmountZero",
    msg: "Auction cannot have a maximum bid amount of 0"
}, {
    code: 6030,
    name: "BidAmountTooHigh",
    msg: "Bid amount is above the maximum bid amount"
}, {
    code: 6031,
    name: "LowerMaxAmountAfterStart",
    msg: "Cannot lower the max bid amount after auction start"
}, {
    code: 6032,
    name: "KeysNotEqual",
    msg: "Keys not equal"
]
```